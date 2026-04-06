# BDG_Intro_to_Server_Environment_and_Architectures  

Student Name: Lim Ka Jun

Student ID: CT0391262  

===================================================================  
# 1. Session 1  
 
* Downloading VmWare Workstation Player (https://www.broadcom.com/)
  * Look for Support Portal located on the top right of the webpage. 
  * Login/Register for an account
  * After logging in click onto this link (https://support.broadcom.com/group/ecx/downloads)
* Download Ubuntu from official Website (https://ubuntu.com/download/desktop)
  * Download the Ubuntu 24.04.4 LTS
* Set up a GitHub account and create a new repository on GitHub

## Lab 1  (Exploring Ubuntu Desktop and CLI Tools)  

### The Basic Tools

* `pwd` prints working directory

  - This shows the full path of your current working directory
 
* `ls` display files and directories in the current working directory (of a specified path).
  - This shows all visible files and folders in the current directory.
    + `ls -l` long listing format: shows permissions, owneer, size, and modification date.
    + `ls -la` list all files (including hidden ones) in long format.
    + `ls -lah` same as `ls -la` but adds human-readable file size (KB, MB, GB instead of raw bytes)
    + `ls -a` shows all files, including hidden ones (those files starting with `.`)
    + `ls -t` sort by modification time (newest first)
    + `ls -S` sort by file size (largest first)
    + `ls -alt` shows all file in long format, sorted by time
    + `ls -ld` shows detailed information about a directory itself, not its content

* `cd` switches your shell session to a new directory
  - `cd ..` moves you one level to the parent directory
  - `cd ~`  moves you to the home directory (regardless of where you are)

* `man` shows manual
  - `man ls` shows manual of ls
  - `man man` shows manual of manual
  - `man + (function)` opens the manual page for that command

* `ping` is used to test network connectivity between computer and another device (like a server, website, or IP address)
* `mkdir` command used in Linux to create new directories (folders)
* `echo` used to print text or variable to the terminal
  - `echo "Text" > fileName.fileType` creates file if it doesn't exist, also content will be overwritten


<img width="881" height="596" alt="image" src="https://github.com/user-attachments/assets/c1de4df9-d083-4223-8e91-37e4f2424608" /> 
<br/>
<br/>
<br/>
<img width="811" height="575" alt="image" src="https://github.com/user-attachments/assets/a138e91d-e001-43f4-b83f-10150a006850" /> 
<br/>
<br/>
<br/>
<img width="811" height="575" alt="image" src="https://github.com/user-attachments/assets/61b41066-0c45-442e-8514-66a577189f8f" />
<br/>
<br/>
<br/>
<img width="813" height="286" alt="image" src="https://github.com/user-attachments/assets/83f3f04e-4a6c-401a-b2fe-034d2a4e7021" />



### Directory Commands

* `ps -e` used to list all the running processes that is on the system.
  - `ps` this command is used to display a snapshot of currently running process.
  - `top` this command shows running processes, CPU usage, memory consumptions, and system load averages in a continuously updating dashboard
    + Under `top` there are many more controls that can be used for example:
      * `q` > Quit
      * `k` > Kill a process by entering its PID
      * `r` > Renice(Change priority) of a process.
      * `M` > Sort by memory usage
      * `h` Help menu with all commands
      * `1` > Display the usage for each individual CPU core.

<br/>

### Create/Edit/View files  
* `touch` creates an empty file or update the timestamp of an exisiting file
* `gedit` edit files with menu/buttons (desktop use)
* `nano` enable quick edit inside terminal
* `cat` print small files directly
* `less` scoll through large files
* `cp` copies files or directories
*  `mv` moves files or directories, or renames them
*  `rm` deletes files or directories

<br/>

### Super User and Permissions  
* `whoami` simply prints the username of the account that is currently logged in as
* `sudo whoami` runs `whoami` with root privileges
* `su` switches user (commonly to root if no username is given)
* `sudo -i` open a root shell (every command runs as root until exit)
* `chmod` change file permissions (read/write/execute)
* `sudo chown (user) (file).(fileType)` change file owner
* `sudo chgrp` changes the group associated with a file or directory

<img width="807" height="579" alt="image" src="https://github.com/user-attachments/assets/efbea229-f434-46d0-ac29-fdd56b8c9128" />

<br/> 

### Linux Services 
* `systemctl list-units --type=service` show a list of all active systemd services on Linux machine
* `sudo systemctl start|stop [service]` controlling services with systemd
  - `sudo systemctl start [service]` start a service
  - `sudo systemctl stop [service]` stop a service
  - `sudo systemctl status [service]` check status a service
  - `sudo systemctl restart [service]` restart a service
  - `sudo systemctl enable [service]` enable auto-start at boot for service
  - `sudo systemctl disable [service]` disable auto-start at boot for service
* `find /path -name "fileName"` to locate file
  - `find /path "*.fileType"` shows all .fileType under path
  - `find /path -type d` used to search for directories.
* `grep` used to search for specific words, phrases, or patterns inside text files or command input, and prints the matching line
  - `grep "text" fileName.txt` prints whole line with search text highlighted
  - `grep -i "Text" fileName.txt` prints whole line with search text highlighted, but is not case-sensitive
  - `grep "Text" *` searched every file in the current folder for line containing search text

<img width="924" height="154" alt="image" src="https://github.com/user-attachments/assets/b05b17fb-340a-4d2d-be7b-a8bb7c46bfd9" />
<br/>
<br/>
<br/>
<img width="918" height="312" alt="image" src="https://github.com/user-attachments/assets/72863a30-cc8b-45df-bcd6-9a01c73451a9" />
<br/>
<br/>
<br/>
<img width="928" height="480" alt="image" src="https://github.com/user-attachments/assets/11f2268c-9950-4001-a907-41fdac820a18" />
<br/>
<br/>
<br/>
<img width="975" height="163" alt="image" src="https://github.com/user-attachments/assets/ee86b7ff-1f1a-45f6-9928-90c86ffab3ff" />
<br/>
<br/>

# 2. Session 2

### Total Cost Of Ownership (TCO)



























