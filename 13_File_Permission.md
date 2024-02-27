### Introduction to File Permissions:

In Unix-like systems, each file and directory has three sets of permissions: one for the owner of the file, one for the group associated with the file, and one for all other users. These permissions determine who can read, write, or execute the file.

### Types of Permissions:

There are three basic types of permissions:

1. **Read (r)**: Allows a user to read the contents of a file or list the contents of a directory.
2. **Write (w)**: Allows a user to modify the contents of a file or create, rename, or delete files in a directory.
3. **Execute (x)**: Allows a user to execute a file as a program or search a directory and access its contents.

### Permission Denied Examples:

- **Read Denied**: If a user doesn't have read permission on a file, attempting to read its contents will result in a "Permission Denied" error.
- **Write Denied**: If a user doesn't have write permission on a file, attempting to modify it or save changes to it will result in a "Permission Denied" error.
- **Execute Denied**: If a user doesn't have execute permission on a file, attempting to execute it as a program will result in a "Permission Denied" error.

### How to Check Permissions of Files:

You can check the permissions of files and directories using the `ls` command with the `-l` option. This will list detailed information about each file, including its permissions. Here's an example:

```bash
ls -l filename
```

This command will display the permissions of the file `filename`.

### How to Change Permissions using chmod:

The `chmod` command is used to change the permissions of files and directories. It can add or remove permissions for the file owner, group, and others. Here's how to use it:

```bash
chmod who+permissions filename
```

- **who**: Specifies who the permission change applies to. It can be one of the following:
  - `u` (user/owner)
  - `g` (group)
  - `o` (others)
  - `a` (all, equivalent to `ugo`)
- **+**: Indicates that permissions are being added.
- **permissions**: Specifies the permissions to be added. It can be one or more of the following:
  - `r` (read)
  - `w` (write)
  - `x` (execute)

Similarly, you can use `-` instead of `+` to remove permissions.

### Examples:

Let's say we have a file named `example.txt` with the following permissions:

```bash
-rw-r--r-- 1 user1 group1 100 Feb 21 12:00 example.txt
```

- To add execute permission for the user:
  ```bash
  chmod u+x example.txt
  ```
- To remove write permission for the group:
  ```bash
  chmod g-w example.txt
  ```
- To add read and execute permissions for all:
  ```bash
  chmod a+rx example.txt
  ```

### Summary:

- **Read Permission (r)**: Allows reading or listing contents.
- **Write Permission (w)**: Allows modifying or creating files.
- **Execute Permission (x)**: Allows executing as a program or accessing contents of a directory.
- **Permission Denied**: Errors occur when attempting actions without appropriate permissions.
- **Checking Permissions**: Use `ls -l filename` to view permissions.
- **Changing Permissions**: Use `chmod who+permissions filename` to add permissions and `chmod who-permissions filename` to remove permissions.

Understanding and managing file permissions is essential for controlling access and ensuring security in Unix-like systems.
