    1.	Explain the difference between absolute path and relative path:
Absolute path states the full path name starting from the root (/). Always start from the root. Example: /home/user/Downloads/file name
Using this file can be accessed from anywhere in the file system.
Relative path specifies the path name starting from the current directory. Always start with a subdirectory. Example: downloads/filename.
This path is relative to /home/user directory because the Downloads directory is located inside the /home/user directory.
    2.	Why Linux uses / instead of \ for its directory paths?
For most parts Linux follow Unix tradition, and so it used forward slash rather than backward slash.

    3.	In Windows, these files are all the same: File FILE file and FiLE. But in Linux this is not the case, Why?
Linux allows this because they’re technically not named exactly the same.

    4.	What is the Filesystem Hierarchy Standard (FHS) and who maintains it?
Linux organizes its files in what is called a hierarchical directory structure (tee-like pattern of folders). FHS specifies requirements and guidelines for a file and directory placement in UNIX-like operating system.

    5.	Explain what type of files are stored in the following directories:
Directory	What is it used for?
/bin	: it is used by system administrators, users, and scripts, and can be accessed :  in single user mode. The basic functions are stored here. 
/dev	: Contains devices files, such as CD/DVD-ROM drive.
/etc	: Contains files that are local to machine.
/home	: It is a user’s home directory.
/lib	: It contains shared libraries that are loaded when a program starts.
/opt	: Contain static shareable add-on software packages.
/tmp	: Contains the temporary files, which are deleted when the system is booted.
/var	: Contains variable data files.
/proc	: It holds all the details about you Linux System. 
/usr	: Contains sharable, read-only applications and files.

    6.	How does a period at the beginning of a file name means (example .bashrc)?
It means the file or directory is hidden, and you cannot see in the file explorer.

    7.	Which command would you use to list all the files inside the /usr/share/ directory?
Ls command

    8.	If you are working in the /usr/share/icons directory and want to move to your home directory, which command would you use?
Cd command

    9.	Explain what these commands do:
cd .config/.htop: 
cd ../: takes you to home directory
ls -lX: long list all the files in a directory

    10.	John has a lot of files in the directory /var/www/html/webapp. He wants to long list all the files, including hidden files, by modification time (newest first), and with human-readable file sizes. Which command should he use conjuring that his current working directory is:
/home/john/.git/ : ls -alht 
