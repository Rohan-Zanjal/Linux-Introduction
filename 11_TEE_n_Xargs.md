## 1. TEE Command:

The tee command is used in Linux to read from the standard input and write to both the standard output and
one or more files simultaneously. It allows users to redirect the output of a command to a file while still
displaying it in the terminal.

#####  Syntax:

```
command | tee [OPTIONS] [FILE...]
```

##### Options:

```-a```: Append to the given files rather than overwriting them.
```-i```: Ignore interrupt signals.
```--help```: Display help information and exit.
```--version```: Display version information and exit.

##### Example:
Suppose you want to list the files in a directory and save the output to a file while still displaying 
it in the terminal. You can achieve this using tee:

```
ls | tee file_list.txt
```

In this example:

* ```ls``` lists the files in the current directory.
* ```tee file_list.txt``` redirects the output of``` ls ```to both the terminal and a file named ```file_list.txt```.


## 2. XARGS Command:

The xargs command is used to build and execute command lines from standard input.
It reads data from the standard input or a file and converts it into arguments for a specified command.
```xargs``` is particularly useful for executing commands that do not accept input directly from standard input.

##### Syntax:

```
xargs [OPTIONS] [COMMAND [INITIAL-ARGS]]
```

##### Options:

```-0```: Use null characters (\0) as the separator instead of whitespace.
```-a file```: Read input from file instead of standard input.
```-n max-args```: Use at most max-args arguments per command line.
```-P max-procs```: Run up to max-procs processes at a time.


##### Example:
Suppose you have a list of filenames in a text file, and you want to delete all these files.
You can use xargs to execute the rm command for each filename listed in the file:

```
xargs rm < file_list.txt
```

In this example:

* ```xargs``` reads the list of filenames from the file ```file_list.txt```.
* ```rm``` (the specified command) is executed for each filename listed in the file, effectively deleting each file.
* 

| Case                                                                        | Description                                 | Command                        |
|-----------------------------------------------------------------------------|---------------------------------------------|--------------------------------|
| TEE Command                                                                 | Redirect output to multiple destinations    |``` command ```                       |
| XARGS Command                                                               | Execute a command with arguments from input | ``` echo arg1 arg2```                 |
