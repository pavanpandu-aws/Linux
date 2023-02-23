# Linux  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRbi9aVFq2CV5UxsEhDk4L5Hk_u4nHnSTnsWhnOUNRg4mfdOfWZfJoPGLZL01QvgvIDT8Q&usqp=CAU" width="25" >

> *Linux* is a free and open-source operating system based on the Unix operating system. It is known for its stability, security, and flexibility, and it has become the most popular operating system for servers and supercomputers.

## 1.File Management

- ls       : used to list the files and directories(*excluding hidden files*)
- cat      : used to display the contents of a file. It can also be used to add the data into the file.
- more     : used to to display the contents of a file one screen at a time.
- tail     : used to display last few lines of the file
- tail -f  : used to to display the last few lines of a file. This is useful for monitoring log files and other files that are updated frequently.
- locate   : used to find files by name. It uses a database of file names and locations to quickly find files.
- cd       : used to change from one directory to another specified directory
- touch    : used to create a new empty file and can also adds the data into the file
- mkdir    : used to create a new directory
- move     : used to move or rename the files and directories
- rm       : used to remove the files and directories
- rmdir    : used to remove an empty directory

- vi       : used to create, edit, and modify text files.
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
  
- cp : used to copy the files nd directories from one location to another.
- cp -r : used to recursively copy a directory and its contents to another location.
- cp -rp : used to recursively copy a directory and its contents to another location, while preserving the permissions and timestamps of the original files and directories. 
- sed : used to perform text transformations on a file or input stream. It can be used to search for a particular pattern and replace it with another pattern. 
- find : to search for files and directories based on various criteria.
  - size : To find files based on their size *-size*
  - date : To find files based on their date *-mtime*
  - keyword : To find files based on a specific keyword, *-name*
- grep : used to search for patterns in files or standard input. It stands for "global regular expression print".
- grep -i : used to search for a keyword in a case-insensitive manner
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
- export : used to create an environment variable
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

## 5.Log Management

- #### Syslog
> *Syslog* is a standard protocol used to log messages from different software applications and system services. It is a way to centralize logging across multiple servers and applications, making it easier to manage and troubleshoot issues.

- #### Journalctl
> *Journalctl* is a command-line utility used to query and view logs collected by the systemd journal. It can be used to search for specific log messages, filter logs based on different criteria, and view logs in various formats.

- #### Custom logs
> *Custom logs* refer to log messages that are generated by custom applications or scripts. It can contain any type of information, from debug messages to application-specific metrics, and are used to help developers and system administrators monitor and troubleshoot their applications.

## 6.Network management

> - **Internal network** refers to the network of devices within an organization or a specific location.
	
> - **External network** refers to the network outside of the organization or location, typically the internet.
	
- A **subnet** is a portion of a larger network
	- A **private subnet** is a subset of IP addresses reserved for use within a private network.They are are typically used for internal communication within an organization.
	 - A **Public subnet** is assigned globally unique IP addresses and can be accessed from the internet. They are used for internet-facing services.
	
- **Ports**

	In computer networking, a port is a communication endpoint for sending and receiving data.
	- **Well-known ports**: *Well-known ports* are predefined and registered with the Internet Assigned Numbers Authority (IANA). They range from 0 to 1023 and are used by commonly recognized services, such as HTTP (port 80), HTTPS (port 443), FTP (port 21), SSH (port 22), Telnet (port 23), and SMTP (port 25).
	- **Registered ports**: *Registered ports* are those in the range of 1024 to 49151. They can be used by applications upon registration with the IANA, but are not as commonly recognized as well-known ports. Examples include Oracle database (port 1521), MySQL (port 3306), and Windows Remote Desktop Protocol (port 3389).
	- **Dynamic or private ports**: *Dynamic or private ports* are those in the range of 49152 to 65535. They are used by the operating system or applications for temporary communication between network endpoints, and are not registered with IANA. These ports are usually assigned by the operating system when a connection is established.
	- **Ephemeral ports**: *Ephemeral ports* are dynamic ports that are assigned by the operating system to a client application when it initiates a connection to a server. These ports typically range from 49152 to 65535, and are used to facilitate communication between the client and server.
	
> - **CIDR** (*Classless Inter-Domain Routing*) is a method of IP address allocation that allows for more efficient use of the available IP address space. *CIDR range calculations* are used to determine the network and host portions of an IP address and subnet mask pair, and to calculate the range of IP addresses that belong to a particular network.
	

> - **HTTP** (Hypertext Transfer Protocol) is a protocol used to transmit data over the internet.
	
> - **HTTPS** (Hypertext Transfer Protocol Secure) is a secure version of HTTP that uses encryption to protect the data transmitted between the web server and the client.
	
	
> - **TCP** (*Transmission Control Protocol*) and **UDP** (*User Datagram Protocol*) are two transport layer protocols used for sending data over IP networks. 
	- TCP provides reliable, ordered, and error-checked delivery of data 
	- UDP provides a faster and simpler connectionless communication.
	

- ifconfig : used to configure and view network interface parameters such as IP address, netmask, broadcast address, and network interface status
	
## Application/Web Servers:
- An application or web server is a software program that runs on a computer to serve web applications, web pages, or other network services to client devices.
	- A **web server** is designed to deliver static and dynamic content over the web for delivering content quickly and efficiently. It typically handles client requests for web pages or files, and responds with the appropriate content. Examples of web servers include *Apache HTTP Server*, *NGINX*, and *Microsoft IIS*.
	- An **Application server** is designed to host and manage web applications that require more complex functionality, such as processing user input, managing session data, and communicating with backend databases or other systems. Examples of application servers include *Apache Tomcat*, *JBoss*, and *IBM WebSphere*.
	
## Load Balancing:
> *Load balancing* is a technique used to distribute network traffic across multiple servers or network resources by preventing overload on individual servers and maintaining uptime. Load balancers typically use algorithms to distribute traffic based on factors such as server availability, current traffic levels, and geographic location.

## High Availability:
> *High Availability* (HA) refers to the ability of a network or network infrastructure to maintain its availability and uptime even in the face of failures or outages. The goal of HA is to ensure that critical services or applications remain accessible to users, even if one or more components of the network fail.

- ##### There are several ways to achieve high availability in a network, including

	- **Redundancy**: This involves duplicating critical components of the network, such as switches, routers, or servers, so that if one fails, another can take over without interruption to service.
	- **Load balancing**: This involves distributing traffic across multiple servers or paths to prevent any single server or path from becoming overloaded or unavailable.
	- **Failover**: This involves automatically switching to a backup or secondary system in the event of a failure or outage. For example, if a primary server fails, a secondary server can automatically take over to ensure continuity of service.
	- **Network virtualization**: This involves creating virtual instances of network devices or services, which can be moved or migrated between physical devices as needed to ensure continuous service.
