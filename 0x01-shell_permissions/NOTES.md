# Shell Permisions

**DevOps** **Shell** **Bash**

# About shell permissions

In Linux, "shell" refers to a command-line interface (CLI) program that allows users to interact with the operating system by executing commands. The shell interprets the commands entered by the user and communicates with the operating system to perform the requested actions.

There are several shell programs available in Linux, including:

- Bash (Bourne Again SHell): The default shell for most Linux distributions.
- Zsh (Z Shell) 
- Ksh (Korn Shell)

Regarding "permissions" in Linux, each file and directory has associated permissions that define which users can perform specific actions on them. Linux uses a permission system that includes three levels of access:

Read (r*4*): Allows the user to view the contents of a file or list the contents of a directory.
Write (w*2*): Grants the user the ability to modify or delete a file, as well as create, rename, or delete files within a directory.
Execute (x*1*): Permits the user to execute a file or access a directory.
The permissions are assigned to three categories of users:

*Owner*: The user who owns the file or directory.
*Group*: Users who belong to the same group as the owner.
*Others*: All other users who do not fall into the above categories.
For each category, the permissions can be set to either allow or deny the corresponding access level (read, write, or execute).

The permissions are represented by a series of characters in Linux file listings. For example, "rwxr-xr--" represents the following:

The first "rwx" indicates the permissions for the owner.
The next "r-x" represents the permissions for the group.
The final "r--" signifies the permissions for others.
By manipulating the file permissions, you can control who can perform actions on the file or directory, enhancing the security and privacy of your system

*--------------------**man or help:**--------------------*


man or help:

1. *chmod* -> Changes the permissions of a file or directory.
2. *sudo* -> Executes a command with superuser (administrative) privileges.
3. su: Switches the user to another user account or superuser.
4. chown: Changes the owner of a file or directory.
chgrp: Changes the group ownership of a file or directory.
id: Displays the user and group identity of the current user.
groups: Lists the groups a user belongs to.
whoami: Displays the username of the current user.
adduser: Adds a new user account to the system.
useradd: Creates a new user account.
addgroup: Adds a new group to the system.

*--------------------**Permissions**--------------------*

*What do the commands chmod, sudo, su, chown, chgrp do*
chmod: The chmod command is used to change the permissions of a file or directory in Linux. It allows you to grant or revoke read, write, and execute permissions for the owner, group, and other users.

sudo: The sudo command stands for "superuser do" and allows a user to execute a command with the privileges of the superuser (usually the root user). It is commonly used to perform administrative tasks that require elevated privileges.

su: The su command, short for "switch user," allows you to switch to another user account or the superuser account (root) by entering the password of the target user. This command is typically used to open a new shell session as a different user.

chown: The chown command is used to change the owner of a file or directory in Linux. It allows you to assign ownership to a specific user or group.

chgrp: The chgrp command is used to change the group ownership of a file or directory. It allows you to assign ownership to a specific group.
*Linux file permissions*
In Linux, each file and directory has permissions that define who can read, write, and execute it. The permissions are divided into three sets: owner, group, and other.

To represent each set of permissions as a single digit, you assign a value to each permission:

Read (r) has a value of 4.
Write (w) has a value of 2.
Execute (x) has a value of 1.
*How to represent each of the three sets of permissions (owner, group, and other) as a single digit*
Then, you sum up the values of the respective permissions for each set. For example:

Owner: read (4) + write (2) + execute (1) = 7.
Group: read (4) + execute (1) = 5.
Other: read (4) + execute (1) = 5.
Therefore, if the owner has read, write, and execute permissions, the group and other users have read and execute permissions, the representation would be "755"
*How to change permissions, owner and group of a file*
*To change permissions*, you can use the chmod command followed by the desired permissions in symbolic or numerical notation. For example, to give read and write permissions to the owner, and read-only permissions to the group and other users:
example - *chmod* 644 filename

*To change the owner of a file*, you need superuser privileges. You can use the chown command followed by the new owner's username:
example - sudo *chown* new_owner filename

 *change the group ownership*
 example - sudo chgrp new_group filename




*Why can’t a normal user chown a file*
Normal users cannot change the owner of a file because it requires administrative privileges. Only the superuser (root) or a user with appropriate permissions (such as using sudo) can change the owner of a file.
*How to run a command with root privileges*

To run a command with root privileges, you can use the sudo command followed by the command you want to execute. For example: sudo command_name

*How to change user ID or become superuser*

To change the user ID or become the superuser, you can use the su command followed by the username or "root". For example, to become the root user: su root


*---------**Other man pages**----------*

*How to create a user*
*How to create a group*
*How to print real and effective user and group IDs*
*How to print the groups a user is in*
*How to print the effective userid*
