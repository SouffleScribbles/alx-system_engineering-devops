# 0x00. Shell, basics

**DevOps** **Shell** **Bash** 

# Learning Objectives
*------------------------------------------------------------*
**man or help**

1. *cd* Used to change the current working directory.
2. *ls* Used to list files and directories in the current directory.
3. *pwd* Displays the current working directory.
4. *less* A pager used to view the contents of a file. It allows scrolling and searching within the file.
5. *file* Determines the file type of a given file.
6. *ln* Creates links between files or directories.
7. *cp* Copies files and directories from one location to another.
8. *mv* Moves or renames files and directories.
9. *rm* Removes (deletes) files and directories.
10. *mkdir* Creates a new directory.
11. *type* Displays information about a command, indicating whether it is a shell built-in, an alias, or an external command.
12. *which* Shows the path of the executable associated with a given command.
13. *help* Provides basic help and usage information for shell built-in commands.
14. *man* Displays the manual pages for various commands, providing detailed information and usage instructions.
*------------------------------------------------------------------------------------------------------------------------*
**General**

*What does RTFM mean?*
RTFM" is an acronym that stands for "Read The Fucking Manual" (or sometimes "Read The Fine Manual").
*What is a Shebang*
* "Shebang," also known as a "hashbang" or "pound-bang," refers to the characters "#!" at the beginning of a script file in Unix-like operating systems.
* The shebang line is used to specify the interpreter or command that should be used to execute the script. 
*It helps the operating system identify the correct interpreter to use for executing the script's commands.
* For example, a shebang line like #!/bin/bash indicates that the script should be executed using the Bash interpreter.
*------------------------------------------------------------------------------------------------------------------------*
**What is the shell?**

*What is the Shell*
* a shell is a command-line interface that allows users to interact with the operating system by executing commands. 
* It acts as an intermediary between the user and the underlying operating system, interpreting and executing commands entered by the user.
*What is the difference between a terminal and a shell*
* A terminal, also known as a console or command prompt, is a program or interface that allows users to access and interact with the shell. It provides a text-based interface for entering commands and receiving their output.
* The terminal communicates with the shell, relaying user commands and displaying the resulting output or responses from the shell.

*To distinguish between the two:*

* Shell: The shell is the command-line interpreter that processes and executes commands. It provides a set of features and functionalities for interacting with the operating system.
* Terminal: The terminal is the program or interface through which users interact with the shell. It provides a text-based environment for entering commands and receiving their output.

*What is the shell prompt*
* The shell prompt is the text or symbol displayed by the shell in the terminal, indicating that it is ready to receive commands.
*How to use the history (the basics)*
* The history command is used to view and manage the command history in most shells. It allows you to access and rerun previously executed commands. 
*------------------------------------------------------------------------------------------------------------------------*
**Navigation**

*What do the commands or built-ins cd, pwd, ls do*
* cd: The cd command is used to change the current working directory in the shell. It allows you to navigate to different directories within the file system.
* pwd: The pwd command stands for "print working directory." It displays the current working directory, which is the directory you are currently located in. 
* ls: The ls command is used to list the contents of a directory
*How to navigate the filesystem*
* cd /: Changes to the root directory.
* cd ..: Moves up one directory (to the parent directory).
* cd directory_name: Changes to the specified directory, assuming it is located in the current directory.
*What are the . and .. directories*
*  . represents the current directory 
* .. represents the parent directory (the directory one level above the current directory).
*What is the working directory, how to print it and how to change it*
* The working directory refers to the directory in which the user is currently located. To print the working directory, you can use the pwd command.
*  To change the working directory, you can use the cd command followed by the desired directory path.
*What is the root directory*
* Root directory: The root directory, denoted by /, is the top-level directory in the file system hierarchy. It is the starting point from which all other directories and files are organized.
*What is the home directory, and how to go there*
* Home directory: The home directory is the default directory for a specific user. It is represented by ~ or $HOME. To navigate to the home directory, you can use cd without any arguments or cd ~.
*What is the difference between the root directory and the home directory of the user root*
* Difference between root and home directory of the user root: The root directory, denoted by /, is the system-wide root directory that contains all other directories and files. The home directory of the user "root" refers to the home directory of the superuser "root," which is typically /root in Unix-like systems.
*What are the characteristics of hidden files and how to list them*
* Hidden files: Hidden files in Unix-like systems are files that have filenames starting with a dot (.). These files are not displayed when using the ls command without any additional options. To list hidden files, you can use the -a option with the ls command, like ls -a or ls -al for a detailed listing.
*What does the command cd - do*
* cd -: The cd - command is used to switch to the previous working directory. It is a shortcut for changing to the directory you were in before the current one. Running cd - will change the working directory to the previous directory you were in.
*------------------------------------------------------------------------------------------------------------------------*
**Looking Around**

*What do the commands ls, less, file do*
*How do you use options and arguments with commands*
*Understand the ls long format and how to display it*
*What does the ln command do*
*What do you find in the most common/important directories*
*What is a symbolic link*
*What is a hard link*
*What is the difference between a hard link and a symbolic link*

 # reference - chat gpt
*-----------------------------------------------------------------------------------------------------------------------*
**Manipulating files**

*What do the commands cp, mv, rm, mkdir do*
*What are wildcards and how do they work*
*How to use wildcards*


# reference - chat gpt
*---------------------------------------------------------------------------------------------------------------------*
**Working with commands**

*What do type, which, help, man commands do*
* type: The type command is used to determine how a command would be interpreted by the shell. It provides information about whether the command is a built-in shell command, an external command, an alias, or a function. For example, type ls would display the type of the ls command.

* which: The which command is used to locate the executable file associated with a given command. It shows the path to the command's executable file. For example, which ls would display the path to the ls command.

* help: The help command is a built-in command in many shells that provides help information about shell built-in commands. It displays a summary of available commands and their usage. For example, help cd would display help information about the cd command.

* man: The man command is used to display the manual pages (documentation) for various commands and topics in Unix-like systems. It provides detailed information about command usage, options, examples, and more. For example, man ls would display the manual page for the ls command.
*What are the different kinds of commands*
* Shell built-in commands: These are commands that are built into the shell itself. They are executed within the shell's process and provide basic functionality.
* External commands: These are standalone executable programs located in directories specified by the PATH environment variable. They are separate from the shell and are executed as separate processes.
* Aliases: Aliases are custom shortcuts or alternative names for commands or command sequences. They are created by users to simplify and customize their command usage.
* Functions: Functions are reusable code blocks defined within the shell. They allow users to create custom commands or perform more complex operations.
*What is an alias*
* Alias: An alias is a user-defined shortcut or alternative name for a command or command sequence. It allows users to create their own customized commands by assigning a shorter or more memorable name to a longer or complex command. Aliases are typically created in the shell's configuration file (e.g., .bashrc or .zshrc).
*When do you use the command help instead of man*
* Using help instead of man: You would typically use the help command instead of man for built-in shell commands. The help command provides quick access to the documentation and usage information specific to the shell's built-in commands. It is often faster and more convenient than searching through the comprehensive manual pages provided by man.
*------------------------------------------------------------------------------------------------------------------------*
**LTS**

*What does LTS mean?*
* LTS stands for "Long-Term Support." It is a term commonly used in the software industry to designate specific releases or versions of software that receive extended support and maintenance.
*------------------------------------------------------------------------------------------------------------------------*








