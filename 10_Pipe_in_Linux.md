
## What is a Pipe in Linux?

In Linux, a pipe, represented by the vertical bar symbol |,
is a form of redirection that allows the output of one command to be passed as input to another command.
It facilitates the chaining of multiple commands together in a single command line, 
allowing for more complex and efficient data processing.

#### Linux Pipe Syntax:

The syntax for using a pipe in Linux is:

```command1 | command2```

Here, command1 generates some output, which is then "piped" (passed) as input to command2.

#### How to Use Linux Pipe in a Command Line:

###### Using a pipe in the command line is straightforward. Here's how it works with an example:

For example, let's use the ls command to list files in the current directory and 
then pass that list to the grep command to search for a specific file:

```ls | grep example.txt```


In this example:

ls lists all files in the current directory.
The output of ls is passed as input to grep.
grep searches for lines containing "example.txt" in the output received from ls.


Explanation:

Pipes are powerful tools in Linux that enable the construction of complex command pipelines.


They are commonly used to:

1. Filter and process large amounts of data.
2. Combine multiple commands to perform complex tasks.
3. Simplify command line operations by breaking them into smaller, more manageable steps.
4. Enable collaboration between different commands and utilities by allowing them to work together seamlessly.

Overall, pipes enhance the flexibility and efficiency of the Linux command line, 
allowing users to manipulate data and perform tasks in a more streamlined manner.


| Case                                                                        | Description                                 | Command                        |
|-----------------------------------------------------------------------------|---------------------------------------------|--------------------------------|
| Case1                                                                       | Find the number of files in a folder        | ```ls -1 ```                        |
| Case2                                                                       | Combine two files and sort them             | ```cat file1.txt file2.txt ```      |
| Case3                                                                       | Find unique data from a file                | ```sort file.txt ```                |
| Case4	                                                                      | See a range of lines in a file              |	```sed -n 'start_line,end_linep' file.txt```  |
| Case5                                                                       | Use More and Less command                   |``` more file.txt or less file.txt``` |


Descriptions:

Case1: Find the number of files in a folder

Description: Counts the number of files in a folder using ```ls``` to list files and ```wc -l``` to count lines.


Case2: Combine two files and sort them

Description: Concatenates two files together using cat and then sorts the combined output using ```sort```.



Case3: Find unique data from a file

Description: Sorts the contents of a file and then extracts unique lines using ```uniq```.



Case4: See a range of lines in a file

Description: Uses ```sed``` to print a specific range of lines from a file.



Case5: Use More and Less command

Description: Use either ```more``` or ```less``` to paginate through a file. 
```more``` shows one page at a time, whereas ```less``` allows backward navigation too.
