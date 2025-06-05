![image](https://github.com/user-attachments/assets/328cfe15-54f4-4dea-a313-801b3eeded64)


![image](https://github.com/user-attachments/assets/af5d4a6e-02e7-4a3e-81fb-fd5d3d4bda98)


## Operating System:
- An operating system (OS) is a system software that manages computer hardware and software resources 
- and acts as an intermediary between the user and the hardware.


## Linux vs Windows

| Feature               | Linux                                | Windows                              |
|-----------------------|---------------------------------------|---------------------------------------|
| Interface             | CLI (Command Line Interface)         | GUI (Graphical User Interface)        |
| Usability             | Difficult to use                     | Easy to use                           |
| Source Code           | Open Source                          | Closed Source                         |
| Licensing             | No Licensing Required                | Licensing Required                    |
| Cost                  | Free                                 | Paid                                  |
| Resource Usage        | Lightweight (Consumes Less Resources)| Heavy (Consumes More Resources)       |
| Security              | More Secure                          | Less Secure                           |





**Linux architecture has four main components hardware,kernel,shell and user/application**



**Hardware:** it consists of motherboard ,CPU,HDD etc

**Kernel:** kernel is the heart/core of the OS, kernel communicates with Hardware

**Shell:** provides interface to user to communicate with kernel 

**Application/user:** Users interact with the system through varies applications such as office, games, etc. 



    
---



## Linux Basic Commands:

**switch to root user**
````
sudo -i
````
**shows username**
````
whoami
````
**shows hostname**
````
hostname
````
**shows present working dir**
````
pwd
````
**display os informaton**
````
cat /etc/os-release
````
**display kernel information**
````
uname -a
````
**display memory information**
````
free -h
````
**display disk information**
````
df -h
````

**list files and dir's**
````
ls
````

**change directory**
````
cd <dirname>
````
**back to previous dir**
````
cd ..
````
- check current shell
````
echo $SHELL
````
- exit the terminal
```bash
exit
```
- check live processes
````
top
````
- check CPU information
```bash
lscpu
```
- check disk/storage information
````
df -h
````
- list block devices
```bash
lsblk
```
- check size of file/dir
````
du -sh file/dirname
````
---

## Directory  Structure in  Linux:

-In Linux directory structure   “/”  (slash) is main directory
- All other directories comes under “/” directory.




1. / - The main folder.


2. /bin - Basic commands everyone uses (e.g., ls, cp).


3. /sbin - Commands for system admins (e.g., reboot).


4. /usr - Programs and tools for users.


5. /var - Stores changing files like logs.


6. /tmp - Temporary files that auto-delete.


7. /etc - System settings and configuration files.


8. /dev - Files that connect to hardware (e.g., USB).


9. /proc - Info about running programs and the system.


10. /sys - Details about hardware and devices.


11. /lib - Helper files for programs to run.


12. /boot - Files needed to start the computer.


13. /home - Personal files for each user.


14. /opt - Extra programs you install.


15. /root - Personal files for the admin.


16. /media - Automatically mounted drives (e.g., USB).


17. /mnt - Manually mounted drives.


18. /srv - Files for server programs (e.g., websites).


19. /run - Temporary system files from this boot.
