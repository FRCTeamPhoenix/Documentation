# Toolchain Setup

In order to work on robotics code, there are a number of programs that need to be properly installed on your machine. These steps will guide you throught the process of setting up everything you need to in order to be ready to develop for the coding subteam.

## Git

Git is the [version control software](https://en.wikipedia.org/wiki/Version_control) used by Team Phoenix, and in order to push changes you make to our repositories, you will need to have it installed on your computer.

#### Windows

1. Grab the windows installer from [here](https://git-scm.com/download/win)

2. Open it, and go through the steps of installing with all of the default options

#### Mac OS X

1. Grab the Mac OS X installer from [here](http://brantsteele.net/hungergames/disclaimer.php)

2. Open it, and go through the steps of installing with all of the default options

3. Ensure your line endings are prroperly configured by running this command in a terminal:

  ```bash
  git config --global core.autocrlf input
  ```

#### Linux

1. Open a command prompt
2. Use your favorite package manager to install Git. On Ubuntu, the command is this:
  
  ```bash
  sudo apt-get install git
  ```
  
3. After the installation finishes, make sure that your line endings are set up correctly by running this command:

  ```bash
  git config --global core.autocrlf input
  ```
  
## Java

The development environment we use, Eclipse, is built on Java, which means that in order to use it Java has to be present on your system. if you already think you have Java installed, feel free to skip this step, but if Eclipse fails to install, you probably need to come back here.

#### Windows

1. Download the latest Windows JDK for your CPU architecture from [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

2. Click on it and go through the steps of installing it, making note of the directory it installs to

3. Set your system PATH variable to include your Java installation:
  
  - Search for "environment variable" in the start menu and click on "Edit the system environment variables"
  - Click the "Environment Variables" button
  - On the top section of the new window, highlight `PATH` and hit "Edit"
  - Press the "New" button to create a new entry, and then enter the path to the `bin` folder inside of your Java installation. For Java 8 Update 64, this should be `C:\Program Files\Java\jdk1.8.0_74\bin`. However, yours may be slightly different.
  - Click "OK" on all of the settings windows to close them
  
#### Mac OS X

1. Download the latest Mac OS X JDK from [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

2. Double click on the file to launch it

3. A Finder window will appear containing an icon of an open box and the name of the .pkg file Double click the package icon to launch the Install app.

4. Go through the installation as you would for any other program
  
#### Ubuntu

1. Add the repository with prebuild Oracle Java installers and update your sources list:

  ```bash
  sudo add-apt-repository ppa:webupd8team/java
  sudo apt-get update
  ```
  
2. Install Java. Make sure to accept the license when prompted.

  ```bash
  sudo apt-get install oracle-java8-installer
  ```

3. Set up Java environment variables by installing this package:

  ```bash
  sudo apt-get install oracle-java8-set-default
  ```
  
## Eclipse

Eclipse is the development environment supported by FIRST, so it's what we use for all robot development. These steps will guide you through getting it set up for the first time. The steps are mostly the same for all operating systems, so there won't be any categories.

1. Download the appropriate installer for your operating system from [here](https://eclipse.org/downloads/index.php?show_instructions=TRUE)

2. Run the executable, and install Eclipse. Make sure you select "Eclipse IDE for C/C++ Developers" when prompted to make a choice

3. Eclipse should be installed. Open it to configure settings

4. Install the WPILib FRC plugins:
    
  ![Image showing steps](https://raw.githubusercontent.com/FRCTeamPhoenix/Documentation/master/images/eclipse-plugin-add.png)
    
  - Select "Help"
  - Click "Install new software".
  - From here you need to add a software update site, the location where the plugins will be downloaded. Push the "Add..." button then fill in the "Add Repository" dialog with:
  - Name: FRC Plugins
  - Location: http://first.wpi.edu/FRC/roborio/release/eclipse/
  - Click "OK".

5. Configure code style. This is mandatory for submitting code to team repositories.

  - Open the preferences window by going to `Window --> Preferences`
  - Navigate to the C++ code style section by going to `C/C++ --> Code Style --> Formatter
  - Select `BSD/Allman [built-in]`, then hit "Edit"
  - At the top of profile editing screen, rename the profile to something else, like "Phoenix Robotics" or "Team 2342"
  - Under general settings, change the tab policy to spaces only, and keep the indentation size at 4
  - Under indent, make sure that all of the options are checked except for "Empty lines" and "Declarations within 'namespace' definition".
  - Hit OK and then OK again to close all windows

## FRC Toolchain

To deploy code to the robot, The WPILib toolchain must be present on your computer. These instructions explain how to install it.

#### Windows/Mac OS X

Download the installer from [here](http://first.wpi.edu/FRC/roborio/toolchains/), run it, and follow the steps to complete the install.

#### Ubuntu

1. Add the repository and update your sources:

  ```bash
  sudo apt-add-repository ppa:wpilib/toolchain
  sudo apt update 
  ```
  
2. Install the toolchain:

  ```bash
  sudo apt install frc-toolchain
  ```
  
## Troubleshooting

Sometimes things won't work on certain systems. Here are some common problems with solutions:

- Eclipse installer not opening/working — Ensure that Java is installed properly according the instructions in this document. If it is, make sure you downloaded installers for the same architecture. For example, if you downloaded an x86 JDK, you must also download an x86 Eclipse installer.
