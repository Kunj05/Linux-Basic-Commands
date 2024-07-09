# Linux Command Line
## Navigate Directories

### Linux File System Tree:
<p align="center"><img src="./images/Linux File System.png" height="450" width="auto"></p>

- **bin**: binary (commands and utilities that all users can run)
- **sbin**: this directory contains programs that performs vital system tasks (network management, disk partitioning). Only the superuser has access to these programs.
- **home**: each user is given a directory under the home directory. A user can store anything in his home directory
- **opt**: optional (additional software)
- **tmp**: temporary files, files created by various programs 
- **var**: variable data, data that frequently changes over time.
# Linux Commands In One Place

## Navigation Commands

- `pwd`: Display the current working directory.
  - Example:
    ```bash
    $ pwd
    /home/john
    ```

- `ls`: List files and directories in the current directory.
  - Example:
    ```bash
    $ ls
    Desktop  Documents  Downloads  Music  Pictures  Videos
    ```

- `ls -l`: Display file/directory information in long format.
  - Example:
    ```bash
    $ ls -l
    total 4
    drwxr-xr-x 2 john john 4096 Jul  9 23:35 Desktop
    ```

- `ls -a`: Display all files/directories, including hidden ones.
  - Example:
    ```bash
    $ ls -a
    .  ..  .bashrc  .profile  Desktop  Documents  Downloads
    ```

- `cd`: Change directory.
  - `cd [directory_name]`: Move to the specified directory.
    - Example:
      ```bash
      $ cd Documents
      ```
  - `cd ..`: Move to the parent directory.
    - Example:
      ```bash
      $ cd ..
      ```
  - `cd ~`: Move to the user’s home directory.
    - Example:
      ```bash
      $ cd ~
      ```

- `mkdir`: Create a new directory.
  - `mkdir [directory_name]`: Create a directory with a specific name.
    - Example:
      ```bash
      $ mkdir new_directory
      ```

## Files and Directories

- `touch [file_name]`: Create an empty file with a specific name.
  - Example:
    ```bash
    $ touch newfile.txt
    ```

- `cp [source] [destination]`: Copy source to destination.
  - Example:
    ```bash
    $ cp file1.txt /home/john/Documents/
    ```

- `mv [source] [destination]`: Move source to destination.
  - Example:
    ```bash
    $ mv file1.txt /home/john/Documents/
    ```
  - `mv [old_name] [new_name]`: Rename a file/directory.
    - Example:
      ```bash
      $ mv oldname.txt newname.txt
      ```

- `rm [file_name]`: Delete a file with a specific name.
  - Example:
    ```bash
    $ rm file1.txt
    ```
  - `rm -r [directory_name]`: Delete a directory and its contents recursively.
    - Example:
      ```bash
      $ rm -r old_directory
      ```

- `cat [file_name]`: Display the contents of a specific file.
  - Example:
    ```bash
    $ cat file1.txt
    This is the content of the file.
    ```

## Text File Manipulation Commands

- `nano` or `vim`: Edit text files in the terminal.
  - Example:
    ```bash
    $ nano file1.txt
    ```

- `echo [text]`: Display text in the terminal.
  - Example:
    ```bash
    $ echo "Hello, World!"
    Hello, World!
    ```
  - `echo [text] > [file_name]`: Save text to a file (overwrite content).
    - Example:
      ```bash
      $ echo "Hello, World!" > file1.txt
      ```
  - `echo [text] >> [file_name]`: Append text to a file (without overwriting).
    - Example:
      ```bash
      $ echo "Hello, again!" >> file1.txt
      ```

## System Information Commands

- `uname`: Display information about the system.
  - Example:
    ```bash
    $ uname
    Linux
    ```
  - `uname -a`: Display detailed system information.
    - Example:
      ```bash
      $ uname -a
      Linux myhostname 5.4.0-42-generic #46-Ubuntu SMP Fri Jul 10 00:24:02 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux
      ```

- `top`: Display a list of running processes.
  - Example:
    ```bash
    $ top
    top - 23:35:01 up  2:29,  1 user,  load average: 0.72, 1.07, 1.04
    Tasks: 174 total,   1 running, 173 sleeping,   0 stopped,   0 zombie
    %Cpu(s):  2.2 us,  0.7 sy,  0.0 ni, 96.8 id,  0.2 wa,  0.0 hi,  0.1 si,  0.0 st
    KiB Mem :  4048172 total,  1512344 free,  1385300 used,  1150528 buff/cache
    KiB Swap:  2097148 total,  2097148 free,        0 used.  2308296 avail Mem 
    ```

- `free`: Display memory usage.
  - Example:
    ```bash
    $ free
                  total        used        free      shared  buff/cache   available
    Mem:        4048172     1512344     1385300       12324     1150528     2308296
    Swap:       2097148           0     2097148
    ```

- `df`: Display disk space usage information.
  - Example:
    ```bash
    $ df
    Filesystem     1K-blocks     Used Available Use% Mounted on
    udev             1998172        0   1998172   0% /dev
    tmpfs             404128     1272    402856   1% /run
    /dev/sda1       30458336 15129504  13853072  53% /
    ```

## User and Permission Management Commands

- `sudo`: Execute commands as a superuser (root).
  - Example:
    ```bash
    $ sudo apt update
    ```

- `useradd`: Add a new user.
  - Example:
    ```bash
    $ sudo useradd newuser
    ```

- `passwd`: Change a user’s password.
  - Example:
    ```bash
    $ sudo passwd newuser
    ```

- `chmod`: Change file/directory permissions.
  - Example:
    ```bash
    $ chmod 755 script.sh
    ```

- `chown`: Change file/directory ownership.
  - Example:
    ```bash
    $ sudo chown john:john file1.txt
    ```

## Networking Commands

- `ping [ip_address]`: Send ICMP echo packets to a network address.
  - Example:
    ```bash
    $ ping google.com
    ```

- `ifconfig` or `ip`: Display network interface information.
  - Example:
    ```bash
    $ ifconfig
    ```
  - Example:
    ```bash
    $ ip a
    ```

- `ssh [username]@[ip_address]`: Connect to a remote machine using Secure Shell (SSH).
  - Example:
    ```bash
    $ ssh john@192.168.1.1
    ```


# General Commands

- `w`: Display information about currently logged in users and what each user is doing.
  - Example:
    ```bash
    $ w
    23:35:01 up  2:29,  1 user,  load average: 0.72, 1.07, 1.04
    USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
    john     :1       :1               21:04   ?xdm?  34:58   0.01s /usr/lib
    ```

- `whoami`: Display the current logged in user's username.
  - Example:
    ```bash
    $ whoami
    john
    ```

- `groups`: Display the groups the user belongs to.
  - Example:
    ```bash
    $ groups
    john adm cdrom sudo dip plugdev lpadmin sambashare
    ```

- `id`: Display user and group information.
  - Example:
    ```bash
    $ id
    uid=1000(john) gid=1000(john) groups=1000(john),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),116(lpadmin),126(sambashare)
    ```

- `hostname`: Display the system's hostname.
  - Example:
    ```bash
    $ hostname
    myhostname
    ```

- `date`: Display or set the system date and time.
  - Example:
    ```bash
    $ date
    Tue Jul  9 23:35:01 UTC 2024
    ```

- `uptime`: Display the system uptime.
  - Example:
    ```bash
    $ uptime
    23:35:01 up  2:29,  1 user,  load average: 0.72, 1.07, 1.04
    ```

- `uname -a`: Display detailed system information.
  - Example:
    ```bash
    $ uname -a
    Linux myhostname 5.4.0-42-generic #46-Ubuntu SMP Fri Jul 10 00:24:02 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux
    ```

- `df`: Display disk space usage information.
  - Example:
    ```bash
    $ df
    Filesystem     1K-blocks     Used Available Use% Mounted on
    udev             1998172        0   1998172   0% /dev
    tmpfs             404128     1272    402856   1% /run
    /dev/sda1       30458336 15129504  13853072  53% /
    ```

- `du`: Display disk usage of files and directories.
  - Example:
    ```bash
    $ du -h
    4.0K    ./Desktop
    1.6G    ./Downloads
    2.1G    ./Documents
    ```

- `free`: Display memory usage.
  - Example:
    ```bash
    $ free
                  total        used        free      shared  buff/cache   available
    Mem:        4048172     1512344     1385300       12324     1150528     2308296
    Swap:       2097148           0     2097148
    ```

- `top`: Display a list of running processes.
  - Example:
    ```bash
    $ top
    top - 23:35:01 up  2:29,  1 user,  load average: 0.72, 1.07, 1.04
    Tasks: 174 total,   1 running, 173 sleeping,   0 stopped,   0 zombie
    %Cpu(s):  2.2 us,  0.7 sy,  0.0 ni, 96.8 id,  0.2 wa,  0.0 hi,  0.1 si,  0.0 st
    KiB Mem :  4048172 total,  1512344 free,  1385300 used,  1150528 buff/cache
    KiB Swap:  2097148 total,  2097148 free,        0 used.  2308296 avail Mem 
    ```

- `ps`: Display currently running processes.
  - Example:
    ```bash
    $ ps
      PID TTY          TIME CMD
    21549 pts/0    00:00:00 bash
    21879 pts/0    00:00:00 ps
    ```

- `kill [pid]`: Terminate a process by its PID.
  - Example:
    ```bash
    $ kill 1234
    ```

- `history`: Display the command history.
  - Example:
    ```bash
    $ history
        1  ls
        2  cd ..
        3  pwd
    ```


