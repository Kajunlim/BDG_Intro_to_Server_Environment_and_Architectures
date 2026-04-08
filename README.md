# BDG_Intro_to_Server_Environment_and_Architectures  

Student Name: Lim Ka Jun

Student ID: CT0391262  

======================================================================================
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

## Lab 2

### Total Cost Of Ownership (TCO)

Assumtions that are made: 
* High performance server on Azure server (~$1500/month) 
* Hardware acquitsition for initial setup ($150,000), operating cost meeting in the middle (~$525) 
* Operate for 5 years (60 Month)
* Have not include maintenance, support, power and cooling
<br/>

|          | Cloud | On-Premises |
| -------- | -------- | -------- |
|Cost for setup| 0 | $205,000 |
|Monthly| $800 | ~$3,417 |
|Yearly | $9,600 | $41,000 |
|3 Years| $28,800 | $$123,000 |
|5 Years| $48,000 | $205,000 |

<br/>
<img width="938" height="856" alt="image" src="https://github.com/user-attachments/assets/ffa88433-5141-4deb-9dc1-66f8e29c4bf3" />
<br/>
<img width="485" height="95" alt="image" src="https://github.com/user-attachments/assets/7dcc288c-2014-425b-9efe-a74d188a3ea9" />
<img width="546" height="138" alt="image" src="https://github.com/user-attachments/assets/f88823ed-28b5-4534-9f58-290004a4776e" />
<br/>
<br/> 

Overall, operating in a cloud would allow companies to save cost as there is no maintenance, support, power and cooling fees in addition to the acquisition cost and operational cost. Furthermore, cloud allows one company to expand or reduce the amount that of storage that they need according to their business model. 
<br/>
<br/>

### Cloud Computing 

* Deployment of VM using Azure server
  - VM Name: azure-webserver
  - Region: Southeast Asia (Zone 1)
  - OS: Linux
* Connections made via Windows Powershell `ssh -i C:\Users\User\Downloads\azureuser.pem <Public Key available on Cloud Service>`
* Basic security hardening 


<br/>
<img width="975" height="920" alt="image" src="https://github.com/user-attachments/assets/4acfa9a0-5b58-4139-8fc2-1477e1a498f1" />
<br/>
<br/>
<br/>
<img width="975" height="999" alt="image" src="https://github.com/user-attachments/assets/709fbd11-47dd-4179-9a0c-5a91bb0b8ccd" />
<br/> 
<br/>
<br/>
<img width="975" height="198" alt="image" src="https://github.com/user-attachments/assets/90f91267-2612-46b2-859e-7efc0de9b3d2" />

### Bash Scripting and Cron
* Create a directory then create a script
  - `mkdir bash` creates a directory
  - `cd bash` goes to the directory created
  - `touch myScript.sh` creates a script
  - `chmod +x myScript.sh`
    + `chmod 777` allows everyone to read, write, and execute the file, `chmod 755` used for script (owner full access, others read/execute only), `chmod 644` used for config files (owner read/write, others read only))

<br/>
<img width="867" height="155" alt="image" src="https://github.com/user-attachments/assets/1ed231ed-acda-457e-8ef1-3d92f38c9b68" />
<br/>
<br/>

* Using loops, if/elif/else, and Cron to evaluate input
  - For Loop
  - if/elif/else
  - use bash to run script
<img width="559" height="227" alt="image" src="https://github.com/user-attachments/assets/0e276d2b-95bf-4383-bc31-ef25998bb005" />
<br/>
<br/>
<img width="985" height="442" alt="image" src="https://github.com/user-attachments/assets/a58a2e2f-986a-42bc-b65e-3daf05eb568a" />
<br/>
<br/>
<img width="534" height="125" alt="image" src="https://github.com/user-attachments/assets/81d76987-e4a1-4b01-86fe-f0b564e7ce10" />
<br/>

# 3. Session 3  

## Lab 3
### Cron job (Basic)
<br/>
<br/>
<img width="975" height="700" alt="image" src="https://github.com/user-attachments/assets/2147b5fb-4dea-4df9-a3b6-585eaf8b9aef" />
<br/>
<br/>
<br/>
<img width="975" height="695" alt="image" src="https://github.com/user-attachments/assets/4a4ff090-f5db-4d21-aee1-faed4516e2f1" />
<br/>
<br/>
<br/>
<img width="731" height="827" alt="image" src="https://github.com/user-attachments/assets/6a85b564-81fa-42fe-8b31-27b364b94abc" />
<br/> 
<br/> 

### Cron job (Lab) 

Cron job is a scheduled task in Linux systems that runs automatically at specified times or intervals, making it essential for autoamting repetive tasks like backups, updates, and monitoring. 

### Original (Lab)
1) Create the directories and test files
2) Create the backup script
3) Code inside the script
4) Upload the PEM key to the VM
5) Fix the key permission on the VM
6) Grant permissions and move the script to /usr/bin
7) Test script manually
8) Check it worked
9) Schedule the cron job (hourly)
10) Test SSH key access to confirm SCP will work

<br/>

```
mkdir -p /home/azureuser/Documents /home/azureuser/backup
echo "test file 1" > /home/azureuser/Documents/file1.txt
echo "test file 2" > /home/azureuser/Documents/file2.txt
mkdir -p /home/azureuser/Documents/subdir
echo "nested file" > /home/azureuser/Documents/subdir/file3.txt

(script)

#!/bin/bash
now=$(date +"%d_%m_%y")

cp -R /home/azureuser/Documents/* /home/azureuser/backup/

zip -r /home/azureuser/$now.zip /home/azureuser/backup/*

cp /home/azureuser/$now.zip /home/azureuser/

scp -i /home/azureuser/azureuser.pem \
    -o StrictHostKeyChecking=no \
    /home/azureuser/$now.zip \
    azureuser@172.188.17.77:/home/azureuser/

(script)

scp -i "C:\Users\User\Downloads\azureuser.pem" "C:\Users\User\Downloads\azureuser.pem" azureuser@172.188.17.77:/home/azureuser/azureuser.pem
chmod 400 /home/azureuser/azureuser.pem
chmod 777 /home/azureuser/testscript.sh
sudo mv /home/azureuser/testscript.sh /usr/bin/testscript
testscript
ls /home/azureuser/*.zip
ls /home/azureuser/backup/
sudo nano /etc/crontab
0 * * * * azureuser /usr/bin/testscript
ssh -i /home/azureuser/azureuser.pem azureuser@172.188.17.77
```


Fixes made: 
scp connections closed
1) Run this in Window PowerShell (Not CMD) 
2) Fix PEM key permissions on Windows. (Windows sometimes blocks the key if it has too many users with access
3) ssh -i "C:\Users\User\Downloads\azureuser.pem" azureuser@172.188.17.77 (If works (SSH is fine), if fails (Go to cloud > see port 22 must be allowed > if missing, add inbound port rule - port 22 to allow)

```
scp -i "C:\Users\User\Downloads\azureuser.pem" "C:\Users\User\Downloads\azureuser.pem" azureuser@172.188.17.77:/home/azureuser/azureuser.pem
icacls "C:\Users\User\Downloads\azureuser.pem" /inheritance:r /grant:r "$($env:USERNAME):(R)"
ssh -i "C:\Users\User\Downloads\azureuser.pem" azureuser@172.188.17.77
```

<br/>

Permission issue on the .pem key file
Common Azure VM issues. Azure VMs typically only allow SSH/SCP using the key from outside, but your trying to SCP from local machine to VM Azure VMs by default disable password authentication and only accept your .pem key for login. 
SCP command needs the key specified correctly on Windows.

1) Run this on Windows PowerShell (Not CMD)
2) Fix PEM key permissions on Windows
3) Verify you can SSH in first

```
chmod 400 /home/azureuser/azureuser.pem
ls -l /home/azureuser/azureuser.pem

(should show on PowerShell)
-r-------- 1 azureuser azureuser ... azureuser.pem
(should show on PowerShell)

ssh -i /home/azureuser/azureuser.pem azureuser@172.188.17.77
```

Unzip the file and change permission (File is zip)
1) Change permission to readable by owner and not writable or executable by anyone.
2) Verify the permission
3) Test again
4) Open/extract the zip
5) Extract into specific folder
6) Check contents
7) Peek without extracting
8) Run the script manually
9) Verify it ran successfully

<br/>

```
chmod 400 /home/azureuser/azureuser.pem
ls -l /home/azureuser/azureuser.pem

(should show on PowerShell)
-r-------- 1 azureuser azureuser ... azureuser.pem
(should show on PowerShell)

ssh -i /home/azureuser/azureuser.pem azureuser@172.188.17.77

Unzip: To run

unzip /home/azureuser/06_04_26.zip
unzip /home/azureuser/06_04_26.zip -d /home/azureuser/extracted/
ls /home/azureuser/extracted/
unzip -l /home/azureuser/06_04_26.zip (Peek without extracting)
testscript
ls /home/azureuser/*.zip
```

<br/>
<img width="975" height="759" alt="image" src="https://github.com/user-attachments/assets/a23a34eb-4bed-4e28-8989-bc6ea23a4209" />
<br/>
<br/>
<br/>
<img width="975" height="819" alt="image" src="https://github.com/user-attachments/assets/3b578629-bbfc-44bf-a986-be13c7d5b453" />
<br/>
<br/>
<br/>
<img width="975" height="828" alt="image" src="https://github.com/user-attachments/assets/1785eeb7-c48b-4d74-9a05-ae2b4a9eae52" />
<br/>
<br/>
<br/>
<img width="975" height="822" alt="image" src="https://github.com/user-attachments/assets/cff4721a-0764-41e7-8904-9091e5ce4c07" />
<br/>
<br/>

### DNS & Certificates
* Register for a free domain at duckDNS (https://www.duckdns.org/)
* Create port 80 (HTTP) and 443 (HTTPS) on your Cloud service
* Connect SSH into your Cloud VM
* Install apache2 `sudo apt update` and `sudo apt install apaache2 -y`
* start apache `sudo systemctl start apache2`
* Change the IP that is defaulted for you at duckDNS (IPv4) to your Public IP
* Verify DNS by using `ping (yourDNSServerName.duckdns.org)`
* Open a web browser and confirm that apache page is running `yourDNSServerName.duckdns.org`


<img width="1035" height="421" alt="image" src="https://github.com/user-attachments/assets/d3b0f6fd-039a-483a-b7e7-00bd53871648" />
<br/>
<br/>

Changed to: 

<br/>
<img width="975" height="448" alt="image" src="https://github.com/user-attachments/assets/7951ba42-bed2-402d-b54c-5eda62e0cfd6" />
<br/>
<br/>
<br/>
<img width="975" height="1208" alt="image" src="https://github.com/user-attachments/assets/72b9da79-395d-4dd6-9cab-360fbdf2bc04" />
<br/>
<br/>

### HTTPS (Secure)
* Installed certbot `sudo apt install certbot python3-certbot-apache`  
* `sudo certbot --apache`  
* HTTPS enabled `https://bdgisea.duckdns.org`  

<br/>
<br/>
<img width="544" height="666" alt="image" src="https://github.com/user-attachments/assets/02532103-461f-4785-8794-25826c7268c0" />
<br/>
<br/>
<br/>
<img width="975" height="1208" alt="image" src="https://github.com/user-attachments/assets/46959d29-ca5a-49d0-9ca7-70479f22f0ef" />
<br/>
<br/>

# 4. Session 4

## Lab 4 (MariaDB)
* Install MariaDB `sudo apt install mariadb-server maria-client -y`
* Start and enable MariaDB service `sudo systemctl start mariadb` then `sudo systemctl enable mariadb`
* Secure MariaDB `sudo mysql_secure_installation`
* Login to MariaDB `sudo mysql -u root -p`
* Query data: 

Sample Used:
```
-- 1. Create a new database
CREATE DATABASE Lab;

-- 2. Switch to the new database
USE Lab;

-- 3. Create a table named 'users'
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    email VARCHAR(100)
);

-- 4. Insert sample rows
INSERT INTO users (name, email) VALUES
('Alice', 'alice@example.com'),
('Bob', 'bob@example.com');

-- 5. Query the table
SELECT * FROM users;
```
<img width="975" height="546" alt="image" src="https://github.com/user-attachments/assets/a4717c7f-d624-4068-8923-f4980092e335" />
<br/>
<br/>
<br/>
<img width="975" height="993" alt="image" src="https://github.com/user-attachments/assets/1a3f72c0-3212-4705-9718-ec34c623f3f5" />
<br/>
<br/>
<br/>
<img width="668" height="582" alt="image" src="https://github.com/user-attachments/assets/a04b74ef-f61c-46bc-94b9-89835ba7c4a3" />
<br/>
<br/>
