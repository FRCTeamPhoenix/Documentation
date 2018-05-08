# Maintaining Personal/Group Forks

In order to maintain a clean central repository, individual programmers can store forks of the central repository to write code in. This document outlines the process required to make this model work.

## Creating a fork

1. Navigate to the central repository via GitHub, and click the 'Fork' button in the top right hand corner of the screen. This will automatically generate a copy of the repository under your name.

2. Follow the steps laid out in [this document](first-pull-into-eclipse.md) to clone the fork on your computer.

3. In your git bash terminal, create a second remote called upstream that points to the central repository, for example:

```bash
git remote add upstream https://github.com/FRCTeamPhoenix/Phoenix2018.git
```

4. Create a new branch and begin writing code. Since this fork is your personal property, feel free to make any tests or changes you need to.

## Syncing a fork

This process will allow you to merge the contents of the current central repository into a branch in your fork. Do this as often as possible to make sure you're working with up-to-date code! *You must have a correctly configured upstream remote in order to sync.*

1. Open Git Bash and navigate to your project directory.

2. Run the following commands to sync your develop branch with the central develop branch.

```bash
git fetch upstream
git checkout develop
git merge upstream/develop
```

3. If merge conflicts are present, resolve them and commit to your local develop branch.

4. Your develop branch is now up to date with the central repository. If you need these changes in another branch, perform a local merge by running:

```bash
git checkout [branch name]
git merge develop
```

## Pull request to central repository

Once you have a working, tested piece of robot code, you are ready to create a *pull request* to the central repository with your code. Following this process correctly is very important to make sure that the central repository remains clean for competitions and demonstrations.

1. **Pull before you push!** Make sure you execute all the instructions in the *Syncing a fork* section and the branch you are pull-requesting contains all the latest changes from the central repository.

2. Create your pull request by navigating to your fork on GitHub, and pressing the 'Create Pull Request' button. This will take you to a screen as shown where you can choose the branch in your fork you are using as well as the branch in the central repository you are merging into.

![pull request](https://raw.githubusercontent.com/FRCTeamPhoenix/Documentation/master/images/pull-request.png)

*Note:* If your pull request window says "Can't automatically merge", it is likely that you have not synced your fork correctly. Make sure to follow this process first.

3. Click 'Create Pull Request' again and give your pull request a title and body based on the template given. *Be descriptive!*

4. A reviewer will be notified of your pull request and review it as soon as possible. Reviewers this year are:

	* [Andrew](https://github.com/denver-blake)

	* [Ian](https://github.com/IanCoolidge0) 

5. Your pull request will be tested in various ways, which will be described in the repository's README file. These include, but are not limited to:

	* Build test (does it compile correctly with our libraries?)

	* Robot test if applicable (does it do what you said it does in the description?)

	* Encapsulation (are central files such as Robot.java and Constants.java mostly unchanged?)

	* Readability (is your code easy to understand?)

6. If all of these standards are met, your pull request will be merged. Congratulations! If one or more of these standards are not met, we will close the pull request and contact you so you can fix the changes.

