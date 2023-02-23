# Linux  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRbi9aVFq2CV5UxsEhDk4L5Hk_u4nHnSTnsWhnOUNRg4mfdOfWZfJoPGLZL01QvgvIDT8Q&usqp=CAU" width="25" >

> Linux is a free and open-source operating system based on the Unix operating system. It is known for its stability, security, and flexibility, and it has become the most popular operating system for servers and supercomputers.

## 1.File Management

- ls       : used to list the files (excluding hidden files)
- cat      : used to view the data and add the data
- more     : used to view the data
- tail     : used to display last line of the file
- tail -f  : used to display the data  which is getting added to the particular file, mostly used to view the logs
- locate   : used to find the path of the specified file
- cd       : used to change from one directory to another specified directory
- touch    : used to create the file and also to adds the information into it
- mkdir    : used to create directory
- move     : used to move or rename the file
- rm       : used to remove the file
- rmdir    : used to remove the directory

- vi       : used to add the information/data to the file
   ###### It has insertion mode and command mode
  - Esc : helps to switch from insertion mode to command mode
  - i   : helps to switch from command mode to insertion mode
  - dd  : used to delete the entire line where cursor placed
  - x   : used to delete the character from where the cursor is placed
  - q!  : used to quit from the vi without saving (!-forcefully)
  - wq! : used to save and quit (!-forcefully)
 
#### Search for a word in vi and replace a word with new word in vi (:%s/oldword/newword/g)

	s- substitue
	%- used to replace the word in the entire file (in all lines)
	g- global search
  
- cp : used to copy the file
- cp -r : used to copy the file recursively
- cp -rp : used to copy the file recursively by preserving the attributes
- sed : used to manage the data in a file (adding or deleting)
- find : used to search the file or directory when we are having 'n' number of files
  - size : acheived by the flag -size
  - date : acheived the flag -mtime
  - keyword : acheived by the flag -name
- grep : used to search for a keyword in the data of a file
- grep -i : used to search for a keyword in insensitive mode
- du : used to display the disk space occupied by files or directories
- df : used to display the disk space availble on the file system
- diff : used to display the differences between two different files
- wc -l : used to display the count of lines in a specified file
- tar : used to archeive the multiple files into a single .tar file
- zip : used to compress the file size which is easy to transfer
- unzip : used to uncompress the file to attain its original file size
- ln : used to create the hard link of the specified file in a specified path
## 2.USER MANAGEMENT

- useradd - : used to create the user
- useradd -m : used to create the home directory for a user
- usermod -aG : used to add a user to an additional group
- usermod -G : used to remove a user from a group
- usermod -s : used to change the login shell of a user
- usermod -d : used to change the home directory of a user
- usermod -l : used to change the username of the user
- usermod -L : used to lock the user
- usermod -U : used to unlock the user
- userdel - : used to delete the user
- userdel -r : used to del the user along with its home directory
- passwd - : used to create/change/update the password for a user
- passwd -d : used to delete the password of a user
- passwd -e : used to force the user to change the password
- passwd -l : used to lock the password of a user
- passwd -u : used to unlock the passsowrd of a user
- passwd -n : used to set the minimum password lifetime to change again

## 3.ACCESS MANAGEMENT

- ssh : used to securely connect to a remote computer or a server and allows secure remote access, file transfer and command execution
- scp : used to securely transfer the files between two linux based systems
- sudo : used to perform administrative tasks without logging in as a root user
- su : used to switch from one user to another user / root user
- chmod : used to change the permissions of a file or directory
- chown : used to change the owner and group of a file or directory

## 4.CONFIGURATION MANAGEMENT

- env : used to display the current environment variables
- PATH : used to specify the list of directories where executable programs are located
- echo : used to prints out a message to the console
- expo :rt : used to create an environment variable
- hostname : used to prints out the name of the current host
- netstat : used to displays the network connections, routing tables and other network interface statistics
- crontab : used to create, view, delete the crontab files which controls the scheduling of commands to be run at specified time
- crontab -e : used to create or edit the crontab file
- crontab -l : used to list the current cron jobs
- kill : used to terminate a process by using pid
- pkill : used to sends a signal to a process based on its name
- wget : used to downloads file from the internet
- curl : used to transfer data between servers using various protocols (HTTPS,HTTPS,SCP)
- ping : used to test the connectivity between two networked devices
- uname : used to prints out system information
- history : used to prints out the historty of the executed commands
- ps : used to displays information about currently running processes
- ps -ux : used to view the list of processes running on the system, including their resource utilization and ownership information
- ps -ef : used to view the process tree hierarchy of all processes 
- ps -ef | grep <pid> : used to view the information about a specific process by its PID

