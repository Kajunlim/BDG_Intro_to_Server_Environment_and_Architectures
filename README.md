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

* `cd` switches your shell session to a new directory
  - `cd ..` moves you one level to the parent directory
  - `cd ~`  moves you to the home directory (regardless of where you are)

* `man` shows manual
  - `man ls` shows manual of ls
  - `man man` shows manual of manual
  - `man + (function)` opens the manual page for that command

* `ping` is used to test network connectivity between computer and another device (like a server, website, or IP address)
* `mkdir` command used in Linux to create new directories (folders)

<img width="881" height="596" alt="image" src="https://github.com/user-attachments/assets/c1de4df9-d083-4223-8e91-37e4f2424608" /> 
<br/>
<img width="811" height="575" alt="image" src="https://github.com/user-attachments/assets/a138e91d-e001-43f4-b83f-10150a006850" /> 
<br/>
<img width="811" height="575" alt="image" src="https://github.com/user-attachments/assets/61b41066-0c45-442e-8514-66a577189f8f" />

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

### Create/Edit/View files  
* `touch` creates an empty file or update the timestamp of an exisiting file
* `gedit` edit files with menu/buttons (desktop use)
* `nano` enable quick edit inside terminal
* `cat` print small files directly
* `less` scoll through large files
* `cp` copies files or directories
*  `mv` moves files or directories, or renames them
*  `rm` deletes files or directories
  

### Super User and Permissions  


























