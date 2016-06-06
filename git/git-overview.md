# Git Overview

### Concepts
Git is a **version control software** which allows teams or individual developers to easily keep track of changes made on a project, and control the way that those changes work their way up to final versions.

- A Git project is hosted remotely, and is called a **repository**
- Git repositories can have one or more **branches**, which all can have different versions of the code in that project. Branches can be merged together or created at any time.
- Conventionally, all projects have a **master** branch, which is typically used for release-ready code.
- Anyone can **clone** a publically available Git repository onto their own computer, and make local changes.
- After changes are made, they can be **committed** locally. Each commit should contain one addition, or fix, and is tagged with an appropriate message.
- Local commits can be **pushed** to the remote Git repository directly
- Users can **fetch** remote changes, which simply downloads the current state of the repository locally.
- After fetching, changes can be **merged** into the working directory.
- When Git fails to automatically merge files from different commits together, a **merge conflict** happens, which needs to be resolved manually.
- Users can **pull** changes from the remote repository, which will perform a **fetch** command and then a **merge** command automatically.

The benefit of using software like Git is that anyone working on the project can easily revert back to a previous commit if something breaks, create a new branch for commits that aren't ready for release, merge changes from multiple people easily, and generally create a safe way for large numbers of people to work on a project together.

### Github

Github is a free hosting platform for Git repositories. In addition to hosting repositories, Github also offers a number of other features that make it the obvious choice for FIRST Robotics teams.

- Online interface for browsing files in repositories
- Pull request system, which allows users to request that their commits be added to a repository, rather than pushing directly
- Tagging commits as releases
- Creating wikis for repositories
- Grouping repositories under the team organization
