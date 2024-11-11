# Linux Journey - Assessment Documentation


# 1. The Shell
### Description:** The shell is a command-line interface that allows users to interact with the operating system by typing commands. Commonly accessed through "Terminal" or "Console" programs, the shell interprets and runs commands you provide.
### Usage:
$ echo Hello World
### Quiz:
Question: What should be outputted to the display when you type echo Hello World?
Answer: Hello World

# 2. pwd (Print Working Directory)
### Description: The pwd command displays the current directory you are in within the filesystem.
### Usage:
$ pwd
### Quiz:
Question: How do I find what directory you are currently in?
Answer: pwd

# 3. cd (Change Directory)
### Description: The cd command lets you change your current directory. You can use both absolute and relative paths to navigate.
### Usage:
$ cd /home/pete/Pictures
### Quiz:
Question: If you are in /home/pete/Pictures and want to go to /home/pete, what shortcut can you use?
Answer: cd ..

# 4. ls (List Directories)
### Description: The ls command lists files and directories in the current or specified directory. Use flags for more details or to view hidden files.
### Usage:
$ ls
$ ls -a
$ ls -l
### Quiz:
Question: What command would you use to see hidden files?
Answer: ls -a

# 5. touch
### Description: touch creates a new, empty file. It can also update the timestamp of an existing file.
### Usage:
$ touch mysuperduperfile
### Quiz:
Question: How do you create a file called myfile?
Answer: touch myfile

# 6. file
### Description: file checks and outputs the file type of a specified file. This is useful since Linux doesn’t require file extensions.
### Usage:
$ file banana.jpg
### Quiz:
Question: What command can you use to find the file type of a file?
Answer: file

# 7. cat
### Description: cat displays the content of files. It can concatenate files and display multiple files' contents together.
### Usage:
$ cat file1.txt
### Quiz:
Question: What's a good way to see the contents of a file?
Answer: cat

# 8. less
### Description: less is useful for reading larger text files, as it allows for page-by-page navigation.
### Usage:
$ less /home/pete/Documents/text1
### Quiz:
Question: How do you quit out of a less command?
Answer: q

# 9. history
### Description: The history command displays previously entered commands. You can re-run commands using arrow keys or shortcuts like !!.
### Usage:
$ history
### Quiz:
Question: What is the command to clear the terminal?
Answer: clear

# 10. cp (Copy)
### Description: The cp command copies files and directories. Use flags like -r for recursive copying and -i for interactive prompts.
### Usage:
$ cp myfile /destination/path
$ cp -r mydirectory /destination/path
### Quiz:
Question: What flag do you need to specify to copy over a directory?
Answer: -r

# 11. mv (Move)
### Description: mv command is used to move or rename files and directories. Similar to cp in terms of flags and functionality, but it doesn’t create a copy.
### Usage:
To rename: $ mv oldfile newfile
To move: $ mv file /target_directory
Use -i flag to prompt before overwriting.
### Quiz
Question: How do you rename a file called cat to dog?
Answer: mv cat dog

# 12. mkdir (Make Directory)
### Description: mkdir creates new directories. The -p option lets you create nested directories in one command.
### Usage:
To create a directory: $ mkdir new_directory
To create nested directories: $ mkdir -p books/authors
### Quiz:
Question: What command is used to make a directory?
Answer: mkdir

# 13. rm (Remove)
### Description: rm deletes files or directories. Be cautious, as deletions are permanent.
### Usage:
To remove a file: $ rm file1
To force remove without prompt: $ rm -f file1
### Quiz:
Question: What flag do you add to forcefully delete a file without a prompt?
Answer: -f

# 14. find
### Description: find is used to search for files and directories in a specified directory hierarchy. It allows searching based on name, type, size, permissions, and other criteria.
### Usage:
To find a file named puppies.jpg in the /home directory:
$ find /home -name puppies.jpg
To search for a directory named MyFolder in /home:
$ find /home -type d -name MyFolder
### Quiz Question: What option should I specify for find if I want to search by name?
Answer: -name

# 15. help 

# 16. man (Manual)
### Description: man displays the manual pages for commands, providing detailed information on their ### Usage, options, and syntax. It’s an essential tool for understanding command functionality.
### Usage:
To view the manual for the ls command:
$ man ls
### Quiz: 
Question:
How do you see the manuals for a command?
Answer: man

# 17. whatis
### Description:The whatis command provides a brief ### Description of a command or program. It pulls a short ### Description from the manual pages.
### Usage:
To get a ### Description of the cat command:
$ whatis cat
### Quiz: 
Question:
What command can you use to see a small ### Description of a command?
Answer: whatis

# 18. alias
### Description: alias allows you to create shortcuts for long commands, making them easier to type and remember. It’s useful for frequently used commands.
### Usage:
To create an alias foobar for ls -la:
$ alias foobar='ls -la'
To remove an alias:
$ unalias foobar
### Quiz: 
Question:
What command is used to make an alias?
Answer: alias

# 19. exit
### Description: exit is used to exit from the current shell session. It terminates the terminal or command-line interface.
### Usage:
To exit the shell:
$ exit
### Quiz:
Question:
How can you exit from the shell?
Answer: exit



