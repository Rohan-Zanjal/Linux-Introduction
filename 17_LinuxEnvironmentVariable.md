### Linux Environment Variables Introduction

In Linux, environment variables are dynamic named values that are stored within the operating system and can affect the behavior of processes and programs running on the system.

### What are Environment Variables?

Environment variables are key-value pairs that define the environment in which programs run. They provide information such as the current user's home directory, preferred text editor, system paths, and more.

### How to View Environment Variables

To view the current environment variables in Linux, you can use the `env` command or the `printenv` command. These commands will display a list of all environment variables and their values.

```bash
env
```

or

```bash
printenv
```

### How to Set Environment Variables

Environment variables can be set using the `export` command followed by the variable name and value.

```bash
export VARIABLE_NAME=value
```

For example:

```bash
export MYVAR="Hello, World!"
```

### Setting Temporary Variables

To set an environment variable temporarily (for the current shell session only), you can use the `export` command without persisting it to configuration files.

```bash
export TEMPVAR="Temporary Value"
```

### Setting Permanent Variables

To set an environment variable permanently (across shell sessions), you need to add the variable definition to the appropriate configuration file. For example, to set it for a specific user, you can add it to the user's `.bashrc` or `.bash_profile` file in their home directory.

```bash
echo 'export PERMVAR="Permanent Value"' >> ~/.bashrc
```

### Setting Variable Globally

To set an environment variable globally (available to all users), you can add it to the system-wide configuration file. Typically, this is done by modifying the `/etc/environment` file.

```bash
sudo echo 'GLOBALVAR="Global Value"' >> /etc/environment
```

### Use Case of Linux Environment Variables

1. **PATH Variable**: Specifies the directories where executable files are located. Allows users to run programs from anywhere in the filesystem.
2. **HOME Variable**: Stores the path to the current user's home directory. Allows easy access to user-specific files and directories.
3. **EDITOR Variable**: Specifies the default text editor to use. Programs use this variable when opening text files for editing.
4. **LANG Variable**: Sets the default language and locale settings for the system.
5. **DISPLAY Variable**: Specifies the display server to use for graphical applications.

Environment variables play a crucial role in configuring and customizing the Linux environment to suit the needs of users and applications. They provide flexibility and control over various aspects of the system's behavior.
