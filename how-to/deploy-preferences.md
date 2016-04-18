**Relevant for 2016 Build Season**

# Deploying the Preferences File to the RIO

1. Open a bash shell and navigate to the directory that has your copy of `networktables.ini`
2. Run `sftp lvuser@roboRIO-(team#)-FRC.local` to connect to the RIO using the SSH File Transfer Protocol
3. Remove any configuration files currently on the RIO by running `rm networktables.ini*`
4. while no driver station is connected, run `put networktables.ini` to transfer your preferences file to the RIO
5. Type `exit` to disconnect

# Viewing current Preferences File on the RIO

1. Open a bash shell
2. Run `ssh lvuser@roboRIO-(team#)-FRC.local` to connect to the RIO using SSH
3. Run `cat networktables.ini` to view the most recent copy of the preferences file
5. Type `exit` to disconnect from the RIO
