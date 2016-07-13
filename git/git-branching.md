# Git Branching

When dealing with a large codebase being worked on by many people, changes made by one person sometimes interfere with changes made by another person. Additionally, teams may want to push features that are not fully completed and that should be kept separate from the production-ready code. This is where Git's branching system comes in. You can think of Git branching as "splitting off" from the main section of the code. Changes can be made to the new branch without altering the main branch that you split off of. When you're satisfied with the state of your code in your branch, you can merge it back in. Here are a couple of common use cases to give you the idea:

- Sally is working on a project which always needs to have stable, ready to use code available. When she wants to start working a on a new feature, which may be unstable or buggy, she creates a new branch for that feature, leaving the stable branch where it is. When the feature is complete and bug-free, she merges it back into the stable branch.
- The release deadline for Google's new messaging app is fast approaching, and even though more features are planned for the future, it's time to start ironing out bugs to prepare for release. A team of programmers creates a new branch in the main Git repository focused only on critical bugfixes for release. No new features are added on this branch, even if there are some new ones added to the repository's master branch. After release, the bugfix branch can be safely merged back into the master branch.

Team Phoenix's branching system makes use of ideas from both of these examples, and a few more.

### Working with Team Phoenix Repositories

*to do*
