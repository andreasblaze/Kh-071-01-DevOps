# Task1.Part1 
## 1) Log in to the system as root. 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.1.jpg)
## 2) Use the passwd command to change the password. Examine the basic parameters of the command. What system file does it change *? 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.2.jpg)
password aging information (and the password itself) is stored in a file /etc/shadow.
## 3) Determine the users registered in the system, as well as what commands they execute. What additional information can be gleaned from the command execution?
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.3.jpg)
Addition info is - username:pswd : uid : gid : uid comments: directory: shell
## 4) Change personal information about yourself. 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.4.jpg)
## 5) Become familiar with the Linux help system and the man and info commands. Get help on the previously discussed commands, define and describe any two keys for these commands. Give examples. 
Info is the default format for documentation inside the GNU project, man is the much older traditional format for UNIX.

man:
-f option: One may not be able to remember the sections in which a command is present. So this option gives the section in which the given command is present.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.5.jpg)
-a option: This option helps us to display all the available intro manual pages in succession.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.6.jpg)
## 6) Explore the more and less commands using the help system. View the contents of files .bash* using commands. 
One of the reasons why less was introduced was to allow backward movement line by line. It has a lot of commands that are similar to the vi text editor’s commands, and it supports horizontal scrolling, live monitoring, and more.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.7.jpg)
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.8.jpg)
more command is used to view the text files in the command prompt, displaying one screen at a time in case the file is large (For example log files). The more command also allows the user do scroll up and down through the page.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.9.jpg)

## 7) * Describe in plans that you are working on laboratory work 1. Tip: You should read the documentation for the finger command. 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.10.jpg)
## 8) * List the contents of the home directory using the ls command, define its files and directories. Hint: Use the help system to familiarize yourself with the ls command. 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.11.jpg)

# Task1.Part2 
## 1) Examine the tree command. Master the technique of applying a template, for example, display all files that contain a character c, or files that contain a specific sequence of characters. List subdirectories of the root directory up to and including the second nesting level. 
The tree is a tiny, cross-platform command-line program used to recursively list or display the content of a directory in a tree-like format. It outputs the directory paths and files in each sub-directory and a summary of a total number of sub-directories and files.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.12.jpg)
## 2) What command can be used to determine the type of file (for example, text or binary)? Give an example.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.13.jpg)
## 3) Master the skills of navigating the file system using relative and absolute paths. How can you go back to your home directory from anywhere in the filesystem? 
Absolute Path - /etc/passwd
Relative Path - Relative path is defined as path related to the present working directory(pwd): pwd/var/logcd kernel
I can go back to my home directory from anywhere in the filesystem using cd ~
## 4) Become familiar with the various options for the ls command. Give examples of listing directories using different keys. Explain the information displayed on the terminal using the -l and -a switches.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.14.jpg)
## 5) Perform the following sequence of operations: - create a subdirectory in the home directory; - in this subdirectory create a file containing information about directories located in the root directory (using I/O redirection operations); 

- view the created file; 
- copy the created file to your home directory using relative and absolute addressing. 
- delete the previously created subdirectory with the file requesting removal; 
- delete the file copied to the home directory. 

![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/1.15.jpg)

## 6) Perform the following sequence of operations: 

- create a subdirectory test in the home directory;

# Task2 
## 1) Analyze the structure of the /etc/passwd and /etc/group file, what fields are present in it, what users exist on the system? Specify several pseudo-users, how to define them?
File  structure   etc / passwd . User  management  starts when  there  are available,i.e / passwd The  / first  you  need  to add  users to the new  system.  There  are several  ways  to do this  task.  Each  of  the methods  modifies  the contents  of  the password  file  / etc etc / passwd file  format  is the same for  all Linux  distros
The filestructure/etc/group. The/etc/groupfileappliestothegeneralsecurity schemeforUnix-likesystems:user,group,andfile access.Theformatforthisfileisasfollows: group_name:password:group_id:list

## 2) What are the uid ranges? What is UID? How to define it? 
uid - password gid : uid comments:  directory: unique  identifier  of  the user  within  the system

## 3) What is GID? How to define it? 
gid shell unique  identifier  of the  group  within  the system  to  which the user  belongs

## 4) How to determine belonging of user to the specific group? 
groups [username]
id [username]

## 5) What are the commands for adding a user to the system? What are the basic parameters required to create a user? 
useradd[-c uidcomment] [-d dir] [-e expire] [-f inactive] [-g gid] [-m [-k skel_dir]] [-s shell] [-u uid[-o]] username
dir-- indicates  to the  user's  home  directory. expire indicates  the  exact  date inactive untill registration  record  are availble . indicates  a continuous number  of days without  registration in  the  system  before  this record  is blocked. gid-- defines  the  id  or  name  of  the  group to  which the  user  belongs. new_username Replaces  the  old  login  name. shell -- defines the shell  for  the  command  interpreter  for  the given user. skel_dir contains  files  which must  be  copied to  the new  user's  home  directory. uid( m is  the  unique  user  identifier  associated  with this  name.indicates  need  to create  a new  home  directory  ( usermod ).---- o g G r ---- Allows  repeating  the  same  user  ID. Select  the  main  group  for  the  login  name. selects  additional  groups. useradd )  or  move  the  current  one  to a new  location Tells  the  user's  home  directory  to  be  moved.  If  the  home  directory  for  the  registration entry  is  out  of date,  existing  files  will  be migrated to the  new  directory.

## 6) How do I change the name (account name) of an existing user?
usermod[-c uidcomment] [-d dir[-m]] [-e expire] [-f inactive] [-g gid] [-G gid[, gid]] [-l new username] [-s shell] [-u uid[-o]] username
usermod -l login-name old-name

## 7) What is skell_dir? What is its structure?
Directory /etc/skel/ (skel is derived from the “skeleton”) is used to initiate home directory when a user is first created.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/2.1.jpg)

## 8) How to remove a user from the system (including his mailbox)? 
userdel -r username

## 9) What commands and keys should be used to lock and unlock a user account? 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/2.2.jpg)

## 10) How to remove a user's password and provide him with a password-free login for subsequent password change? 
### passwd -e user1
### chage -l user1

## 11) Display the extended format of information about the directory, tell about the information columns displayed on the terminal. 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/2.3.jpg)
### Permissions, gid, user, store, mod data and time, directories
## 12) What access rights exist and for whom (i. e., describe the main roles)? Briefly describe the acronym for access rights. 
### The Linux filesystem gives us three types of permissions. Here is a simplified review:
- User (or user owner)
- Group (or owner group)
- Other (everyone else)
### With these permissions, we can grant three (actually five, but we’ll get to that in a minute) types of access:
- Read
- Write
- eXecute

## 13) What is the sequence of defining the relationship between the file and the user? 
### When the relationship between the file and the user who started the process, the role is determined as follows
### If the UID of the file is the same as the UID of the process, the user is the owner of the file
### If the GID of the file matches the GID of any group the user belongs to, he is a member of the group to which the file belongs
### If neither the UID no the GID of a file overlaps with the UID of the process and the list of groups that the user running it belongs to, that user is an outsider

## 14) What commands are used to change the owner of a file (directory), as well as the mode of access to the file? Give examples, demonstrate on the terminal. 
Permissions can be changed using three commands chown (change owner), chgrp (change group), and
chmod with extended parameter format before the access part (before the or sign), can list the
roles " u"," g"," and " a"( which corresponds to ugo for which access is being changed
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/2.4.jpg)

## 15) What is an example of octal representation of access rights? Describe the umask command. 
### The same bitwise representation of attributes regulates the default access rights when creating files and
### directories This is done using the umask command The only umask parameter is an octal number that
### specifies the attributes that should not be set on a new file 666 or directory 777
### For example, umask 0 will cause files to be created with rw rw rw attributes and directories rwxrwxrwx

## 16) Give definitions of sticky bits and mechanism of identifier substitution. Give an example of files and directories with these attributes. 
### Sticky Bit is mainly used on folders in order to avoid deletion of a folder and it’s content by other users though they having write permissions on the folder contents If ### Sticky bit is enabled on a folder, the folder contents are deleted by only owner who created them and the root user No one else can delete other users data in this folder(Where sticky bit is set) This is a security measure to avoid deletion of critical folders and their content(sub folders and files), though other users have full permissions
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/2.5.jpg)
## 17) What file attributes should be present in the command script?
All twelve attributes can be represented as bits of a binary number, equal to 1 if the attribute is set, and 0 if not The order of the bits is as follows sU | sG | t | rU | wU | xU | rG | wG || xG | rO | wO | xO, where sU is SetUID, sG is SetGID, t is a t attribute (ls dl then the directory is displayed as a file), than three triples of access attributes

# Task3
## Part1
## 1. How many states could has a process in Linux?
Two types of processes in Linux: foreground and background
## 2. Examine the pstree command. Make output (highlight) the chain (ancestors) of the current process.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/3.1.jpg)
## 3. What is a proc file system? 
The proc file system acts as an interface to internal data structures in the kernel. It can be used to obtain information about the system and to change certain kernel parameters at runtime (sysctl). 
## 4. Print information about the processor (its type, supported technologies, etc.).
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/3.2.jpg)

## 5. Use the ps command to get information about the process. The information should be as follows: the owner of the process, the arguments with which the process was launched for execution, the group owner of this process, etc.
 ![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/3.3.jpg)

## 6. How to define kernel processes and user processes?
Kernel processes are a part of the Linux kernel, and each of them is started with its own process identification number (PID). When managing processes, it is easy to recognize the kernel processes because they have a name that is between square brackets. Listing shows a list of a few

## 7. Print the list of processes to the terminal. Briefly describe the statuses of the processes. What condition are they in, or can they be arriving in?
PID – the unique process ID 
TTY – terminal type that the user is logged into 
TIME – amount of CPU in minutes and seconds that the process has been running 
CMD – name of the command that launched the process. 
Note – Sometimes when we execute ps command, it shows TIME as 00:00:00. It is nothing but the total accumulated CPU utilization time for any process and 00:00:00 indicates no CPU time has been given by the kernel till now. In above example we found that, for bash no CPU time has been given. This is because bash is just a parent process for different processes which needs bash for their execution and bash itself is not utilizing any CPU time till now. 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/3.4.jpg)
## 8. Display only the processes of a specific user. 
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/3.5.jpg)
## 9. What utilities can be used to analyze existing running tasks (by analyzing the help for the ps command)?
### If you are looking for a short summary of the active processes, use ps aux.
### If you are not only looking for the name of the process but also for the exact command that was used to start the process, use ps ef .
### Alternative ways to use ps exist as well, such as the command ps fax , which shows hierarchical relationships between parent and child
## 10. What information does top command display?
top command is used to show the Linux processes. It provides a dynamic real-time view of the running system. Usually, this command shows the summary information of the system and the list of processes or threads which are currently managed by the Linux Kernel.
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/3.6.jpg)
## 11. Display the processes of the specific user using the top command.
top -U root
![Image](https://github.com/andreasblaze/Kh-071-01-DevOps/raw/main/Linux/img/3.7.jpg)
## 12. What interactive commands can be used to control the top command? Give a couple of examples.
Now that you know how to use the kill and nice commands from the command line, using the same functionality from top is even easier. From top , type k . top will then prompt for the PID of the process you want to send a signal to. By default, the most active process is selected. After you enter the PID, top asks which signal you want to send. By default, signal 15 for SIGTERM is used. However, if you want to insist a bit more, you can type 9 for SIGKILL. Then press Enter to terminate the process. To renice a running process from top, type r . You are first prompted for the PID of the process you want to renice. After entering the PID, you are prompted for the nice value you want to use. Enter a positive value to increase process priority or a negative value to decrease process priority.


## 13. Sort the contents of the processes window using various parameters (for example, the amount of processor time taken up, etc.)
To sort all Linux running processes by Process ID, press M and T keys.
To sort all Linux running processes by Memory usage, press M and P keys.
<Shift> + <N> - sort by PID ;
<Shift> + <P> - sort by CPU usage ;
<Shift> + <M> sort by Memory usage;
<Shift> +<T> sort by Time usage;
<Shift> + <Z> - change colors;
<c> - display absolute path of command;
And more hotkeys are available.

## 14. Concept of priority, what commands are used to set priority?
When Linux processes are started, they are started with a specific priority By default, all regular processes are equal and are started with the same priority, which is the priority number 20 In some cases, it is useful to change the default priority that was assigned to the process when it was started You can do that using the nice and renice commands Use nice if you want to start a process with an adjusted priority Use renice to change the priority for a currently active process Alternatively, you can use the r command from the top utility to change the priority of a currently running process When using nice or renice to adjust process priority, you can select from values ranging from 20 to 19 The default niceness of a process is set to 0 (which results in the priority value of 20 By applying a negative niceness, you increase the priority Use a positive niceness to decrease the priority It is a good idea not to use the ultimate values immediately Instead, use increments of 5 and see how it affects the application
## 15. Can I change the priority of a process using the top command? If so, how? 
### You can change the process priority using nice and renice utility. Nice command will launch a process with an user defined scheduling priority. Renice command will modify the scheduling priority of a running process. Linux Kernel schedules the process and allocates CPU time accordingly for each of them.
### To renice a running process from top, type r . You are first prompted for the PID of the process you want to renice . After entering the PID, you are prompted for the nice value you want to use. Enter a positive value to increase process priority or a negative value to decrease process priority.

## 16. Examine the kill command. How to send with the kill command process control signal? Give an example of commonly used signals.
Now that you know how to use the kill and nice commands from the command line, using the same functionality from top is even easier. From top , type k . top will then prompt for the PID of the process you want to send a signal to. By default, the most active process is selected. After you enter the PID, top asks which signal you want to send. By default, signal 15 for SIGTERM is used. However, if you want to insist a bit more, you can type 9 for SIGKILL. Then press Enter to terminate the process.
## 17. Commands jobs, fg, bg, nohup. What are they for? Use the sleep, yes command to demonstrate the process control mechanism with fg, bg.

## Part2

## 1. Check the implementability of the most frequently used OPENSSH commands in the MS Windows operating system. (Description of the expected result of the commands + screenshots: command – result should be presented)

## 2. Implement basic SSH settings to increase the security of the client-server connection (at least 

## 3. List the options for choosing keys for encryption in SSH. Implement 3 of them.

## 4. Implement port forwarding for the SSH client from the host machine to the guest Linux virtual machine behind NAT.