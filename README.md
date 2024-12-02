Shell Permissions
 Novice
 Weight: 1
 Project will start Dec 2, 2024 12:00 AM, must end by Dec 9, 2024 12:00 AM
 Checker was released at Dec 2, 2024 12:00 AM
 An auto review will be launched at the deadline
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

Permissions
What do the commands chmod, sudo, su, chown, chgrp do
Linux file permissions
How to represent each of the three sets of permissions (owner, group, and other) as a single digit
How to change permissions, owner and group of a file
Why can’t a normal user chown a file
How to run a command with root privileges
How to change user ID or become superuser
Requirements
General
Allowed editors: vi, vim, emacs
All your scripts will be tested on Ubuntu 20.04 LTS
All your scripts should be exactly two lines long ($ wc -l file should print 2)
All your files should end with a new line (why?)
The first line of all your files should be exactly #!/bin/bash
A README.md file, at the root of the folder of the project, describing what each script is doing
You are not allowed to use backticks, &&, || or ;
All your files must be executable
Quiz questions
Great! You've completed the quiz successfully! Keep going! (Show quiz)
Tasks
0. My name is Betty
mandatory
Create a script that switches the current user to the user betty.

You should use exactly 8 characters for your command (+1 character for the new line)
You can assume that the user betty will exist when we will run your script
julien@ubuntu:/tmp/h$ tail -1 0-iam_betty | wc -c
9
julien@ubuntu:/tmp/h$
Repo:

GitHub repository: alx_be_shell
Directory: shell_permissions
File: 0-iam_betty
 
1. Who am I
mandatory
Write a script that prints the effective username of the current user.

julien@ubuntu:/tmp/h$ ./1-who_am_i
julien
julien@ubuntu:/tmp/h$ 
Repo:

GitHub repository: alx_be_shell
Directory: shell_permissions
File: 1-who_am_i
 
2. Empty!
mandatory
Write a script that creates an empty file called hello.

Repo:

GitHub repository: alx_be_shell
Directory: shell_permissions
File: 4-empty
 
3. Execute
mandatory
Write a script that adds execute permission to the owner of the file hello.

The file hello will be in the working directory
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./hello
bash: ./hello: Permission denied
julien@ubuntu:/tmp/h$ ./5-execute 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rwxrw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
Repo:

GitHub repository: alx_be_shell
Directory: shell_permissions
File: 5-execute
 
4. Multiple permissions
mandatory
Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.

The file hello will be in the working directory
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-r--r----- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./6-multiple_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-r-xr-xr-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
Repo:

GitHub repository: alx_be_shell
Directory: shell_permissions
File: 6-multiple_permissions
 
5. John Doe
mandatory
Write a script that sets the mode of the file hello to this:

-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
The file hello will be in the working directory
You are not allowed to use commas for this script
Repo:

GitHub repository: alx_be_shell
Directory: shell_permissions
File: 9-John_Doe
