# Lab Report 3

## Task
> Consider the commands less, find, and grep. Choose one of them. Online, find 4 interesting command-line options or alternate ways to use the command you chose. For example, we saw the -name option for find in class. For each of those options, give 2 examples of using it on files and directories from ./technical. Show each example as a code block that shows the command and its output, and write a sentence or two about what it’s doing and why it’s useful.

## grep -l
searches for a specific pattern in one or more files and outputs the names of the files that contain a match, rather than displaying the matching lines themselves. It is particularly useful when you want to quickly identify the files that contain a specific pattern without displaying the actual content of those files. This option is often combined with other grep options to refine the search.

## grep -n
searches for a specific pattern in one or more files and outputs the matching lines along with their line numbers. 

## grep -C
Also known as grep --context, allows you to specify the number of lines of context to display before and after each match. It helps provide additional context around the matching lines, making it easier to understand the context in which the pattern occurs.

## grep -r
The -r stands for "recursive," and it allows you to search files and directories recursively.
