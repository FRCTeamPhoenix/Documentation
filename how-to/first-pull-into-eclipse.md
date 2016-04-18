**Relevant for all years**

# First Pull Into an Eclipse Project
#### Instructions for Robot C++

These steps will allow you to set up an Eclipse project that will be synced with a team repository, letting you pull from it and commit changes. This assumes that the Eclipse workspace is at `C:\Users\YOUR_USERNAME\workspace`, where `YOUR_USERNAME` is your username. It also assumes that you can connect to `github.com`. Git Bash is the shell used for these steps and the example repository that we'll pull will be [Phoenix2016](https://github.com/FRCTeamPhoenix/Phoenix2016).

In Eclipse:

1. Go to `File --> New --> Project`
2. Choose "Example Robot C++ Project" and pick a simple example, like "Mecanum Drive". The actual project doesn't matter, we'll be deleting the source files before we pull
3. Click next, and use the name of the repository you want to pull as the name of the project
4. Click finish.

Exit Eclipse and open up the git bash shell or something similar:

5. Navigate to your Eclipse workspace:

    ```bash
    cd "/c/Users/YOUR_USERNAME/workspace/PROJECT_NAME"
    ```
    Where `YOUR_USERNAME` is your username and `PROJECT_NAME` is the name of the    project you just created

6. Remove the sample code from the project, since we're pulling everything off of GitHub:

    ```bash
    rm src/Robot.cpp
    ```
    
7. Initialize git in your project directory. Replace the URL in the second line with the URL you get by pressing this button on the repository you want to pull from:

    ![Screenshot of Copy to Clipboard Button](https://raw.githubusercontent.com/FRCTeamPhoenix/Documentation/master/images/copy-to-clipboard.PNG)
    
    Now run these commands in order (The URL being used for example purposes is from the Phoenix2016 repository):
    
    ```bash
    git init
    git remote add origin https://github.com/FRCTeamPhoenix/Phoenix2016.git
    git fetch
    git checkout -t origin/master
    ```
    
8. Reopen Eclipse and right click on your project. Select `Team --> Share Project`, hit next, then hit finish.

9. If you followed all of the steps correctly, you should now be able to right click the project in Eclipse, scroll down to `Team`, and perform various Git operations, such as pulling and pushing.
