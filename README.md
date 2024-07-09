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
- `ls`: List files and directories in the current directory.
- `ls -l`: Display file/directory information in long format.
- `ls -a`: Display all files/directories, including hidden ones.
- `cd`: Change directory.
  - `cd [directory_name]`: Move to the specified directory.
  - `cd ..`: Move to the parent directory.
  - `cd ~`: Move to the user’s home directory.
- `mkdir`: Create a new directory.
  - `mkdir [directory_name]`: Create a directory with a specific name.

## Files and Directories

- `touch [file_name]`: Create an empty file with a specific name.
- `cp [source] [destination]`: Copy source to destination.
- `mv [source] [destination]`: Move source to destination.
  - `mv [old_name] [new_name]`: Rename a file/directory.
- `rm [file_name]`: Delete a file with a specific name.
  - `rm -r [directory_name]`: Delete a directory and its contents recursively.
- `cat [file_name]`: Display the contents of a specific file.

## Text File Manipulation Commands

- `nano` or `vim`: Edit text files in the terminal.
- `echo [text]`: Display text in the terminal.
  - `echo [text] > [file_name]`: Save text to a file (overwrite content).
  - `echo [text] >> [file_name]`: Append text to a file (without overwriting).

## System Information Commands

- `uname`: Display information about the system.
  - `uname -a`: Display detailed system information.
- `top`: Display a list of running processes.
- `free`: Display memory usage.
- `df`: Display disk space usage information.

## User and Permission Management Commands

- `sudo`: Execute commands as a superuser (root).
- `useradd`: Add a new user.
- `passwd`: Change a user’s password.
- `chmod`: Change file/directory permissions.
- `chown`: Change file/directory ownership.

## Networking Commands

- `ping [ip_address]`: Send ICMP echo packets to an IP address.
- `ifconfig` or `ip`: Display network interface information.
- `ssh [username]@[ip_address]`: Connect to a remote machine using Secure Shell (SSH).

# General Commands

- `w`: Display who is logged on and what they are doing.
- `whoami`: Display the current logged in user's username.
- `groups`: Display the groups the user belongs to.
- `id`: Display user and group information.
- `hostname`: Display the system's hostname.
- `date`: Display or set the system date and time.
- `uptime`: Display the system uptime.
- `uname -a`: Display detailed system information.
- `df`: Display disk space usage information.
- `du`: Display disk usage of files and directories.
- `free`: Display memory usage.
- `top`: Display a list of running processes.
- `ps`: Display currently running processes.
- `kill [pid]`: Terminate a process by its PID.
- `history`: Display the command history.
- `clear`: Clear the terminal screen.
- `man [command]`: Display the manual page

