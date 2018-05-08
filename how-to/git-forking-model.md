# Maintaining Personal/Group Forks

In order to maintain a clean central repository, individual programmers can store forks of the central repository to write code in. This document outlines the process required to make this model function.

## Creating a fork

1. Navigate to the central repository via GitHub, and click the 'Fork' button in the top right hand corner of the screen. This will automatically generate a copy of the repository under your name.

2. Follow the steps laid out in [this document] (first-pull-into-eclipse.md) to clone the fork on your computer.

3. In your git bash terminal, create a second remote called upstream that points to the central repository, for example:

```bash
git remote add upstream https://github.com/FRCTeamPhoenix/Phoenix2018.git
```

4. Create a new branch and begin writing code.

## Syncing a fork

This process will allow you to merge the contents of the current central repository into a branch in your fork. Do this as often as possible to make sure you're working with up-to-date code! *You must have a correctly configured upstream remote in order to sync.*

1. Open Git Bash and navigate to your project directory.

2. Run the following commands to sync your develop branch with the central develop branch.

```bash
git fetch upstream
git checkout develop
git merge upstream/develop
```

3. If merge conflicts are present, resolve them and commit to your local develop.

4. Your develop branch is now up to date with the central repository. If you need these changes in another branch, perform a local merge by running:

```bash
git checkout [branch name]
git merge develop
```
