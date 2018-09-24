# VSCode Setup

To install vscode follow the instructions [Here](https://wpilib.screenstepslive.com/s/currentCS/m/79833/l/932382-installing-vs-code )

Also install the VS Code Java extension pack and WPILib VSstat Code extension.

Read [here](https://wpilib.screenstepslive.com/s/currentCS/m/79833/l/941601-vs-code-basics-and-wpilib-in-vs-code) to familiar with VSCode and WPILib extension.


## Git in VSCode

To clone a repository in vscode, open the command palette by pressing Ctrl+Shift+P (Cmd+Shift+P on Mac). Type in "Git:Clone" and press Enter. Enter in the repository URL founded on GitHub.
![Screenshot of Copy to Clipboard Button](https://raw.githubusercontent.com/FRCTeamPhoenix/Documentation/master/images/copy-to-clipboard.PNG)

To use other git commands in vscode, open the command palette by pressing Ctrl+Shift+P (Cmd+Shift+P on Mac). Type in "Git:" and the command name or go to the source control tab

## External Dependencies

Team Phoenix projects should contain a `lib/` directory at the top level. To add an external jar to your classpath (such as Jackson libraries), add the jar file to this directory. A correctly set-up project should add the library automatically to the classpath.


#### Setting Up External Dependencies

As the initial creator (i.e. owner) of a project, when creating the project add a `lib/` directory **AND** add the following line to `build.gradle`:

`compile fileTree(include: ['*.jar'], dir: 'lib')`

The resulting `build.gradle` should have this block:

![Screenshot of build.gradle dependencies](https://raw.githubusercontent.com/FRCTeamPhoenix/Documentation/master/images/external-dependencies.PNG)


