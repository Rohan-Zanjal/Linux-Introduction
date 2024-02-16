#### File System Structure


| Directory | Description                                                                                    |
|-----------|------------------------------------------------------------------------------------------------|
| /boot     | Contains files used by the boot loader, such as GRUB configuration files and kernel images.    |
| /dev      | Holds special files representing system devices, such as hard drives, keyboards, and speakers. |
| /etc      | Stores system configuration files used by various applications and services.                   |
| /usr/bin  | Contains executable binaries (programs) accessible to all users.                               |
| /usr/sbin | Holds system binaries (executable programs) primarily used by the root user.                   |
| /opt      | Used for optional add-on application installations.                                            |
| /proc     | A virtual file system that provides information about running processes and system status.     |
| /usr/lib  | Contains C program library files needed by commands and applications.                          |
| /tmp      | Stores temporary files created by various processes.                                           |
| /home     | Contains home directories for all user accounts.                                               |
| /root     | The home directory for the root user.                                                          |
| /var      | Holds system log files and variable data files, such as mail spools and website content.       |
| /run      | Used for storing temporary runtime files, such as PID files, created by system daemons.        |
| /mnt      | A directory used for manually mounting external file systems, such as NFS shares.              |
| /media    | Typically used as the mount point for removable media, such as CD-ROMs and USB drives.         |






| Component                   | Description                                             | Commands/Examples                                               |
|-----------------------------|---------------------------------------------------------|-----------------------------------------------------------------|
| Boot Block                  | Initial code for booting the operating system           | N/A                                                             |
| Superblock                  | Metadata about the file system                          | dumpe2fs /dev/sda1 (for ext file systems in Linux)              |
| Inode Table                 | Metadata about files and directories                    | ls -i (to display inode numbers in Linux)                       |
| Data Blocks                 | Actual contents of files and directories                | cat file.txt (to display contents of a file)                    |
| Directory Structure         | Organizes files and directories hierarchically          | ls (to list files and directories in a directory)               |
| File Allocation Table (FAT) | Maps clusters to files                                  | fsutil fsinfo sectorinfo C: (for FAT file systems in Windows)   |
| Journal (Optional)          | Log of changes made to the file system                  | tune2fs -l /dev/sda1 (to view journal info in ext file systems) |
| Free Space Management       | Tracks available space and manages allocation           | df -h (to display disk space usage in Linux)                    |
| File System Utilities       | Tools for managing and interacting with the file system | mkdir directory_name (to create a directory)                    |
