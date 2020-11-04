# Linux-Cheatsheet

## User Info


**1. who** : It is used to get information about currently logged in user on the system. It Displays
 - <b>Login name of the user </b>  
 - <b> User terminal </b> 
 - <b> Date & Time of login </b> 
 - <b> Remote host name of the user </b> 
```bash
    $ who
    mohit :0 2020-10-21 01:21 (:0)
```

**2. whoami:** It display the system’s username

```bash
   $ whoami
   mohit
```

**3. users** : Displays usernames of all users currently logged on the system.

```bash
   $ users
   sj
```

**4. last or lastb** : Displays a list of last logged in users on the system. You can pass user names to display their login and hostname details.

```bash
    
    $ last
    mohit       :0           :0               Fri Oct 16 01:27    gone - no logout
    reboot   system boot  5.4.0-29-generic    Thu Oct 15 01:27   still running
    mohit       :0           :0               Wed Oct 14 11:46 - crash (29+13:40)
    reboot   system boot  5.4.0-29-generic    Sat Oct 10 11:45   still running
    mohit       :0           :0               Fri Oct 09 21:04 - crash (75+14:41)
    reboot   system boot  5.4.0-29-generic Thu May 14 21:03   still running
    
    wtmp begins Thu May 14 21:03:56 2020
```


## File Commands

**1. pwd** The pwd command is used to print the current Working Directory

```bash
   $ pwd
   /home/mohit/Desktop/
```

**2. mkdir** The mkdir command is used to make new directory.
```bash
   $ mkdir python
   $ ls
   python
```

**3. rmdir**: The rmdir command is used to remove directories.

```bash
   rmdir FolderName
```

**4. rm**: The rm command is used to remove objects such as files, directories, symbolic links etc from the file system.
1. **remove file:**   
    ```bash
    rm filenamename
    ```

2. **remove file forcefully:**
    ```bash
    rm -f filename
    ```

3. **remove directory**
    ```bash
    rm -r dirname
    ```

**5. touch**: The touch command is is used to create, change and modify timestamps of a file without any content.
   1. **Create new file:** creating new file in the dir.
       ```bash
       touch filename
       ```
   2. **Create multiple files:** creating multiple new files in dir.
       ```bash
       touch file1name file2name file3name
       ```
   3. **Change access time:** Used to change the access time of a file.
       ```bash
       touch -a filename
       ```
   4. **Change modification time:** Used to change the modified time.
       ```bash
       touch -m filename
       ```
   5. **Use timestamp of other file:** Used to get timestamp of another file.
       ```bash
       touch -r file2 file1
       ```
       
**6. cat**: The cat command is used to list the contents of file
```bash
      cat file1name
```


## File Permissions

Linux is Mutliuser Operating system so security is reqiured to prevent people from accesing each other's confidential files.

Linux Divides this authorization in 2 levels-

**1. Ownership**:
- <b>User:</b> Owner of the file who created it.
- <b>Group:</b> Group of users with the same access permissions to the file or directory. 
- <b>Other:</b> Applies to all other users on the system.

**2. Permissions**:
- <b> Read:</b> Give you the authority to open and read a file and lists its content for a directory.
- <b> Write:</b> Give you the authority to modify the contents of a file and add, remove and rename files stored in the directory.
- <b>Execute:</b> Give you the authority to run the program in Unix/Linux.

The permissions are indicated with below characters,

    r = read permission

    w = write permission

    x = execute permission

    \- = no permission


## Networking

**1. Display network information:** `ifconfig` command is used to display all network information(ip address, ports etc)

```bash
ifconfig -a
```

**2. Test connection to a remote machine:** Send an echo request to test connection of a remote machine.
```bash
    ping <ip-address> or hostname
    Example:
    ping 10.0.10.11
```

**3. Show IP Address:** Display ip address of a currennt machine
```bash
    hostname -I
    (OR)
    ip addr show
```

**4. Active ports:** Shows active or listening ports
```bash
     netstat -pnltu
```

**5. Find information about domain:** `whois` command is used to find out information about a domain, such as the owner of the domain, the owner’s contact information, and the nameservers used by domain.
```bash
    whois [domain]
    Example:
    whois google.com
```

**6. Ping:** to check connectivity status (ping google.com)


### System and Hardware information

**1. Print all information**: Used to print system information.
```bash
$ uname -a
```

**2. Print kernel name**:
```bash
$ uname -s
```

**3. Print kernel release**:
```bash
$ uname -r
```

**4. Print Architecture**:
```bash
$ uname -m
```

**5. Print Operating System**:
```bash
$ uname -o
```


## Shutdown

**1. shutdown -h now:** immediately power off & shutdown the system.

**2. shutdown -h +5 :** shutdown the system after 5 minutes.

**3. shutdown -r now:** reboot the system.

**4. shutdown -Fr now:** orce file system check during reboot.


**[⬆ Back to Top](#Linux-Cheatsheet)**