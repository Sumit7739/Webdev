# Linux Command Line Basics

## 1. ls (List)
- **Purpose**: Lists directory contents
- **Usage**: `ls [options] [directory]`
- **Common options**:
  - `-l`: Long format
  - `-a`: Show hidden files
  - `-h`: Human-readable file sizes

```bash
$ ls
Documents  Downloads  Pictures

$ ls -l
total 12
drwxr-xr-x 2 user user 4096 May 15 10:00 Documents
drwxr-xr-x 2 user user 4096 May 15 10:00 Downloads
drwxr-xr-x 2 user user 4096 May 15 10:00 Pictures
```

## 2. pwd (Print Working Directory)
- **Purpose**: Displays the current working directory
- **Usage**: `pwd`

```bash
$ pwd
/home/user
```

## 3. cd (Change Directory)
- **Purpose**: Changes the current working directory
- **Usage**: `cd [directory]`
- **Special directories**:
  - `..`: Parent directory
  - `.`: Current directory
  - `~`: Home directory

```bash
$ pwd
/home/user
$ cd Documents
$ pwd
/home/user/Documents
$ cd ..
$ pwd
/home/user
```

## 4. mkdir (Make Directory)
- **Purpose**: Creates new directories
- **Usage**: `mkdir [options] directory_name`
- **Common option**:
  - `-p`: Create parent directories as needed

```bash
$ mkdir new_folder
$ ls
Documents  Downloads  new_folder  Pictures

$ mkdir -p parent/child/grandchild
$ ls -R parent
parent:
child

parent/child:
grandchild

parent/child/grandchild:
```

## 5. mv (Move)
- **Purpose**: Moves or renames files and directories
- **Usage**: `mv [options] source destination`

```bash
$ touch file.txt
$ ls
file.txt
$ mv file.txt newfile.txt
$ ls
newfile.txt
$ mv newfile.txt Documents/
$ ls Documents
newfile.txt
```

## 6. cp (Copy)
- **Purpose**: Copies files and directories
- **Usage**: `cp [options] source destination`
- **Common option**:
  - `-r`: Copy directories recursively

```bash
$ cp newfile.txt backup.txt
$ ls
backup.txt  newfile.txt

$ cp -r Documents Docs_backup
$ ls
backup.txt  Docs_backup  Documents  newfile.txt
```

## 7. rm (Remove)
- **Purpose**: Removes files and directories
- **Usage**: `rm [options] file/directory`
- **Common options**:
  - `-r`: Remove directories and their contents recursively
  - `-f`: Force removal without prompting

```bash
$ rm backup.txt
$ ls
Docs_backup  Documents  newfile.txt

$ rm -r Docs_backup
$ ls
Documents  newfile.txt
```

## 8. touch
- **Purpose**: Creates empty files or updates file timestamps
- **Usage**: `touch file_name`

```bash
$ touch new_file.txt
$ ls -l
total 0
-rw-r--r-- 1 user user 0 May 15 11:00 new_file.txt
```

## 9. ln (Link)
- **Purpose**: Creates links between files
- **Usage**: `ln [options] target link_name`
- **Common option**:
  - `-s`: Create a symbolic link

```bash
$ ln -s /path/to/file.txt link_to_file
$ ls -l
total 0
lrwxrwxrwx 1 user user 17 May 15 11:05 link_to_file -> /path/to/file.txt
```

## 10. clear
- **Purpose**: Clears the terminal screen
- **Usage**: `clear`

```bash
$ clear
# Terminal screen is now cleared
```

Remember to practice these commands regularly to become proficient in using the Linux command line interface!

---

# More Linux Command Line Tools

Let's expand our Linux command-line knowledge with these crucial tools:

## 1. cat (Concatenate)
- **Purpose**: Displays the contents of files on the terminal
- **Usage**: `cat [options] file1 file2 ...`
- **Common options**:
  - `-n`: Number lines
  - `-b`: Number non-empty lines

```bash
$ cat file.txt
This is the content of file.txt

$ cat -n file.txt
     1  This is the content of file.txt
```

## 2. echo (Echo)
- **Purpose**: Prints any text that follows the command
- **Usage**: `echo [options] string`
- **Common options**:
  - `-e`: Enable interpretation of backslash escapes
  - `-n`: Do not print a trailing newline

```bash
$ echo "Hello, world!"
Hello, world!

$ echo -e "Hello, \nworld!"
Hello,
world!
```

## 3. less (Less)
- **Purpose**: Displays paged outputs in the terminal, allowing you to scroll through large files or outputs
- **Usage**: `less [options] file`
- **Navigation**:
  - `Space`: Scroll down one page
  - `b`: Scroll up one page
  - `Enter`: Scroll down one line
  - `q`: Quit less

```bash
$ less large_file.txt
# You can now scroll through the file using the navigation keys.
```

## 4. man (Manual)
- **Purpose**: Access manual pages for all Linux commands
- **Usage**: `man [command]`

```bash
$ man ls
# Displays the manual page for the 'ls' command.
```

## 5. uname (Unix Name)
- **Purpose**: Gets basic information about the operating system
- **Usage**: `uname [options]`
- **Common options**:
  - `-a`: Display all information
  - `-s`: Display the kernel name

```bash
$ uname -a
Linux hostname 5.10.0-10-amd64 #21~20.04.1-Ubuntu SMP Fri Jul 1 17:06:08 UTC 2022 x86_64 x86_64 x86_64 GNU/Linux

$ uname -s
Linux
```

## 6. whoami (Who Am I)
- **Purpose**: Displays the current user's username
- **Usage**: `whoami`

```bash
$ whoami
user
```

## 7. tar (Tape Archive)
- **Purpose**: Creates, extracts, and manipulates archive files
- **Usage**: `tar [options] [archive-file] [files]`
- **Common options**:
  - `-c`: Create archive
  - `-x`: Extract archive
  - `-t`: List archive contents
  - `-z`: Use gzip compression
  - `-f`: Specify archive file

```bash
$ tar -czvf my_archive.tar.gz file1.txt file2.txt
# Creates a compressed archive named 'my_archive.tar.gz' containing 'file1.txt' and 'file2.txt'

$ tar -xzvf my_archive.tar.gz
# Extracts the contents of the archive.
```

## 8. grep (Global Regular Expression Print)
- **Purpose**: Searches for lines matching a regular expression
- **Usage**: `grep [options] pattern [file]`
- **Common options**:
  - `-i`: Ignore case
  - `-v`: Invert the match (show lines that don't match)

```bash
$ grep "hello" file.txt
# Displays lines in 'file.txt' that contain "hello".

$ grep -i "world" file.txt
# Displays lines containing "world" regardless of case.
```

## 9. head (Head)
- **Purpose**: Displays the first specified number of lines from a file
- **Usage**: `head [options] [number] file`
- **Common option**:
  - `-n`: Specify the number of lines to display

```bash
$ head file.txt
# Displays the first 10 lines of 'file.txt'.

$ head -n 5 file.txt
# Displays the first 5 lines of 'file.txt'.
```

## 10. tail (Tail)
- **Purpose**: Displays the last specified number of lines from a file
- **Usage**: `tail [options] [number] file`
- **Common option**:
  - `-n`: Specify the number of lines to display

```bash
$ tail file.txt
# Displays the last 10 lines of 'file.txt'.

$ tail -n 5 file.txt
# Displays the last 5 lines of 'file.txt'.
```

<!-- Remember, practice is the key to mastering these tools. Explore their options and use them in your daily Linux tasks to become more efficient and comfortable with the command line. -->

---



# Advanced Linux Command Line Tools

Let's dive deeper into the world of Linux command-line tools with these advanced utilities:

## 1. diff (Difference)
- **Purpose**: Finds the difference between two files
- **Usage**: `diff [options] file1 file2`
- **Common options**:
  - `-u`: Unified output format
  - `-c`: Context output format
  - `-q`: Quiet output, only reports if files differ

```bash
$ diff file1.txt file2.txt
# Displays the differences between 'file1.txt' and 'file2.txt'.

$ diff -u file1.txt file2.txt
# Displays the differences in unified format.
```

## 2. cmp (Compare)
- **Purpose**: Compares two files and reports if they are identical
- **Usage**: `cmp [options] file1 file2`
- **Common option**:
  - `-s`: Silent output, only reports if files differ

```bash
$ cmp file1.txt file2.txt
# Reports if 'file1.txt' and 'file2.txt' are identical.

$ cmp -s file1.txt file2.txt
# Silently reports if 'file1.txt' and 'file2.txt' differ.
```

## 3. comm (Common)
- **Purpose**: Combines the functionality of `diff` and `cmp` to compare two files
- **Usage**: `comm [options] file1 file2`
- **Common options**:
  - `-1`: Suppress lines unique to file1
  - `-2`: Suppress lines unique to file2
  - `-3`: Suppress lines common to both files

```bash
$ comm file1.txt file2.txt
# Displays lines unique to 'file1.txt', 'file2.txt', and common to both.

$ comm -1 file1.txt file2.txt
# Suppresses lines unique to 'file1.txt'.
```

## 4. sort (Sort)
- **Purpose**: Sorts the content of a file while outputting
- **Usage**: `sort [options] file`
- **Common options**:
  - `-n`: Sort numerically
  - `-r`: Reverse sort
  - `-u`: Unique sort

```bash
$ sort file.txt
# Sorts the content of 'file.txt' alphabetically.

$ sort -n file.txt
# Sorts the content of 'file.txt' numerically.
```

## 5. export (Export)
- **Purpose**: Exports environment variables in Linux
- **Usage**: `export [variable_name]=[value]`
- **Common usage**:
  - `export PATH=$PATH:/new/path`

```bash
$ export MY_VAR="Hello, world!"
# Exports the environment variable 'MY_VAR' with the value "Hello, world!".

$ echo $MY_VAR
Hello, world!
```

## 6. zip (Zip)
- **Purpose**: Zips files in Linux
- **Usage**: `zip [options] archive_name file1 file2 ...`
- **Common options**:
  - `-r`: Recursively zip directories
  - `-q`: Quiet output

```bash
$ zip my_archive.zip file1.txt file2.txt
# Zips 'file1.txt' and 'file2.txt' into 'my_archive.zip'.

$ zip -r my_archive.zip directory/
# Recursively zips the contents of 'directory/' into 'my_archive.zip'.
```

## 7. unzip (Unzip)
- **Purpose**: Unzips files in Linux
- **Usage**: `unzip [options] archive_name`
- **Common options**:
  - `-q`: Quiet output
  - `-d`: Extract to a specific directory

```bash
$ unzip my_archive.zip
# Unzips the contents of 'my_archive.zip' to the current directory.

$ unzip -d /path/to/directory my_archive.zip
# Unzips the contents of 'my_archive.zip' to '/path/to/directory'.
```

## 8. ssh (Secure Shell)
- **Purpose**: Establishes a secure connection to a remote server
- **Usage**: `ssh [options] user@host`
- **Common options**:
  - `-p`: Specify the port number
  - `-i`: Specify the identity file

```bash
$ ssh user@remote_host
# Establishes a secure connection to 'remote_host' as 'user'.

$ ssh -p 2222 user@remote_host
# Establishes a secure connection to 'remote_host' on port 2222.
```

## 9. service (Service)
- **Purpose**: Manages system services (start, stop, restart, etc.)
- **Usage**: `service [service_name] [action]`
- **Common actions**:
  - `start`: Starts the service
  - `stop`: Stops the service
  - `restart`: Restarts the service

```bash
$ service httpd start
# Starts the 'httpd' service.

$ service httpd stop
# Stops the 'httpd' service.
```

## 10. ps (Process Status)
- **Purpose**: Displays active processes
- **Usage**: `ps [options]`
- **Common options**:
  - `-a`: Displays all processes
  - `-u`: Displays processes owned by the specified user
  - `-x`: Displays processes without a controlling terminal

```bash
$ ps -a
# Displays all active processes.

$ ps -u user
# Displays processes owned by 'user'.
```

<!-- Mastering these advanced Linux command-line tools will take your skills to the next level. Practice using them to become more efficient and proficient in your daily Linux tasks. -->

---

# System Commands

## 1. kill (Kill a Process)
- **Purpose**: Sends a signal to a process to terminate it.
- **Usage**: `kill [signal] [PID]`
- **Common signals**:
  - `SIGTERM` (15): Gracefully stop a process.
  - `SIGKILL` (9): Immediately terminate a process without cleanup.
  - `SIGHUP` (1): Reload a process.

```bash
$ kill -9 1234
# Immediately terminates the process with PID 1234.

$ kill -TERM 1234
# Gracefully stops the process with PID 1234.

$ kill -l
# Lists all available signals.
```

To find the PID, you can use commands like `ps`, `pgrep`, or `pidof`.

## 2. killall (Kill Processes by Name)
- **Purpose**: Terminates processes by their name.
- **Usage**: `killall [signal] process_name`
- **Common usage**:
  - `killall -9 firefox`
    - Immediately terminates all instances of the Firefox process.

```bash
$ killall firefox
# Terminates all Firefox processes with the default SIGTERM signal.

$ killall -9 firefox
# Immediately terminates all Firefox processes.
```

This command is useful for killing multiple processes with the same name without needing to specify each PID.

## 3. df (Display Disk Filesystem Information)
- **Purpose**: Displays information about disk space usage.
- **Usage**: `df [options]`
- **Common options**:
  - `-h`: Human-readable format.
  - `-T`: Display file system type.

```bash
$ df -h
# Displays disk space usage in a human-readable format.

$ df -T
# Displays the type of each file system along with usage information.
```

This command helps you understand how much disk space is used and available on each mounted file system.

## 4. mount (Mount File Systems)
- **Purpose**: Attaches a file system to a directory.
- **Usage**: `mount [options] device_name mount_point`
- **Common options**:
  - `-t`: Specify the file system type.
  - `-o`: Specify mount options.

```bash
$ mount /dev/sdb1 /mnt
# Mounts the device /dev/sdb1 to the /mnt directory.

$ mount -t ext4 /dev/sdb1 /mnt
# Mounts an ext4 file system from /dev/sdb1 to /mnt.
```

This command is essential for making file systems available for use by the operating system.

## 5. chmod (Change File Permissions)
- **Purpose**: Changes the permissions of files or directories.
- **Usage**: `chmod [permissions] file/directory`
- **Common permissions**:
  - `u`: User
  - `g`: Group
  - `o`: Other
  - `r`: Read
  - `w`: Write
  - `x`: Execute

```bash
$ chmod 755 file.txt
# Sets the permissions to rwxr-x (owner has full permissions, group and others have read and execute).

$ chmod u+x file.txt
# Adds execute permission for the owner.
```

This command is used to manage access control for files and directories.

## 6. chown (Change Ownership)
- **Purpose**: Changes the ownership of files or directories.
- **Usage**: `chown [user]:[group] file/directory`
- **Common usage**:
  - `chown user file.txt`
    - Changes the owner of the file to the specified user.
  - `chown user:group file.txt`
    - Changes both the owner and group of the file.

```bash
$ chown user file.txt
# Changes the owner of 'file.txt' to 'user'.

$ chown user:group file.txt
# Changes the owner and group of 'file.txt' to 'user' and 'group', respectively.
```

This command is used to manage file and directory ownership.

## 7. ifconfig (Display Network Interfaces)
- **Note**: `ifconfig` is deprecated in favor of `ip` command in modern Linux systems.
- **Purpose**: Displays network interface information.
- **Usage**: `ifconfig [interface]`
- **Common usage**:
  - `ifconfig eth0`
    - Displays information about the eth0 interface.

```bash
$ ifconfig eth0
# Displays information about the eth0 network interface.
```

For modern systems, use the `ip` command instead:
```bash
$ ip addr show
# Displays detailed information about all network interfaces.
```

## 8. traceroute (Trace Network Hops)
- **Purpose**: Traces the route of packets to a network host.
- **Usage**: `traceroute [options] host`
- **Common options**:
  - `-i`: Specify the network interface.
  - `-n`: Suppress DNS lookups.

```bash
$ traceroute example.com
# Traces the network path to example.com.

$ traceroute -n example.com
# Traces the network path to example.com without performing DNS lookups.
```

This command helps in diagnosing network issues by showing the path packets take to reach a destination.

## 9. wget (Download Files)
- **Purpose**: Downloads files from the internet.
- **Usage**: `wget [options] URL`
- **Common options**:
  - `-b`: Run in the background.
  - `-o`: Specify the output file name.

```bash
$ wget https://example.com/file.txt
# Downloads the file from the specified URL.

$ wget -b https://example.com/file.txt
# Downloads the file in the background.
```

This command is useful for downloading files from the web directly from the command line.

## 10. ufw (Uncomplicated Firewall)
- **Purpose**: Manages the firewall rules in a simple way.
- **Usage**: `ufw [options]`
- **Common options**:
  - `enable`: Enables the firewall.
  - `disable`: Disables the firewall.
  - `allow`: Allows traffic on a specific port or service.
  - `deny`: Denies traffic on a specific port or service.

```bash
$ ufw enable
# Enables the firewall.

$ ufw allow 80
# Allows HTTP traffic on port 80.

$ ufw deny 22
# Denies SSH traffic on port 22.
```

This command is used to manage firewall rules in Ubuntu and other compatible systems.

## 11. iptables (Base Firewall)
- **Purpose**: The base firewall utility that other firewalls interface with.
- **Usage**: `iptables [options]`
- **Common options**:
  - `-A`: Append a rule to a chain.
  - `-D`: Delete a rule from a chain.
  - `-L`: List the rules in a chain.

```bash
$ iptables -A INPUT -p tcp --dport 80 -j ACCEPT
# Allows HTTP traffic on port 80.

$ iptables -D INPUT -p tcp --dport 80 -j ACCEPT
# Deletes the rule allowing HTTP traffic on port 80.

$ iptables -L
# Lists all the current firewall rules.
```

This command is used to manage the underlying firewall rules and is often used by other firewall utilities like `ufw`.

Understanding and using these commands will help you manage various aspects of your Linux system, from process management and file system operations to network diagnostics and firewall configuration.

---

## Package Managers

### 1. `apt` (Advanced Package Tool)
- **Purpose**: Package manager for Debian-based systems (e.g., Ubuntu).
- **Usage**: `apt [options] command`
- **Common commands**:
  - `install`: Install packages.
  - `remove`: Remove packages.
  - `update`: Update the package list.
  - `upgrade`: Upgrade installed packages.

```bash
$ sudo apt update
# Updates the package list.

$ sudo apt install package_name
# Installs the specified package.

$ sudo apt remove package_name
# Removes the specified package.
```

### 2. `pacman` (Package Manager)
- **Purpose**: Package manager for Arch Linux.
- **Usage**: `pacman [options] command`
- **Common commands**:
  - `-S`: Synchronize packages.
  - `-R`: Remove packages.
  - `-Syu`: Sync and update the system.

```bash
$ sudo pacman -Syu
# Synchronizes the package database and updates the system.

$ sudo pacman -S package_name
# Installs the specified package.

$ sudo pacman -R package_name
# Removes the specified package.
```

### 3. `yum` (Yum)
- **Purpose**: Package manager for Red Hat-based systems (e.g., CentOS, Fedora).
- **Usage**: `yum [options] command`
- **Common commands**:
  - `install`: Install packages.
  - `remove`: Remove packages.
  - `update`: Update installed packages.

```bash
$ sudo yum update
# Updates all installed packages.

$ sudo yum install package_name
# Installs the specified package.

$ sudo yum remove package_name
# Removes the specified package.
```

### 4. `rpm` (RPM Package Manager)
- **Purpose**: Package manager for Red Hat-based systems.
- **Usage**: `rpm [options]`
- **Common options**:
  - `-i`: Install a package.
  - `-e`: Remove a package.
  - `-q`: Query the package database.

```bash
$ sudo rpm -i package_name.rpm
# Installs the specified RPM package.

$ sudo rpm -e package_name
# Removes the specified package.

$ rpm -q package_name
# Queries the package database for information about the specified package.
```

## System and User Management

### 5. `sudo` (Superuser Do)
- **Purpose**: Allows a permitted user to execute a command as the superuser.
- **Usage**: `sudo [command]`

```bash
$ sudo apt update
# Executes the 'apt update' command with superuser privileges.

$ sudo useradd new_user
# Adds a new user with superuser privileges.
```

### 6. `cal` (Calendar)
- **Purpose**: Displays a calendar.
- **Usage**: `cal [options]`

```bash
$ cal
# Displays the current month's calendar.

$ cal 2023
# Displays the calendar for the entire year 2023.
```

### 7. `alias` (Alias)
- **Purpose**: Creates custom shortcuts for regularly used commands.
- **Usage**: `alias name='command'`

```bash
$ alias ll='ls -l'
# Creates an alias 'll' for the 'ls -l' command.

$ alias gs='git status'
# Creates an alias 'gs' for the 'git status' command.
```

### 8. `dd` (Disk Dump)
- **Purpose**: Copies data from one file to another, often used for creating bootable USB sticks.
- **Usage**: `dd [options] if=input_file of=output_file`
- **Common options**:
  - `if`: Input file.
  - `of`: Output file.
  - `bs`: Block size.

```bash
$ sudo dd if=/path/to/image.iso of=/dev/sdX bs=4M
# Creates a bootable USB stick from an ISO image.
```

### 9. `whereis` (Where Is)
- **Purpose**: Locates the binary, source, and manual pages for a command.
- **Usage**: `whereis [command]`

```bash
$ whereis ls
# Displays the path to the 'ls' binary and its manual page.
```

### 10. `whatis` (What Is)
- **Purpose**: Displays a brief description of a command.
- **Usage**: `whatis [command]`

```bash
$ whatis ls
# Displays a brief description of the 'ls' command.
```

### 11. `top` (Top)
- **Purpose**: Displays active processes live with their system usage.
- **Usage**: `top`

```bash
$ top
# Opens the top utility, displaying system processes and their resource usage.
```

### 12. `useradd` (User Add)
- **Purpose**: Adds a new user.
- **Usage**: `useradd [options] username`
- **Common options**:
  - `-m`: Create the user's home directory.
  - `-s`: Specify the user's shell.

```bash
$ sudo useradd -m new_user
# Adds a new user with a home directory.
```

### 13. `usermod` (User Modify)
- **Purpose**: Modifies existing user data.
- **Usage**: `usermod [options] username`
- **Common options**:
  - `-aG`: Add the user to supplementary groups.
  - `-s`: Change the user's shell.

```bash
$ sudo usermod -aG sudo new_user
# Adds the user to the 'sudo' group.

$ sudo usermod -s /bin/bash new_user
# Changes the user's shell to bash.
```

### 14. `passwd` (Password)
- **Purpose**: Creates or updates passwords for existing users.
- **Usage**: `passwd [username]`

```bash
$ sudo passwd new_user
# Sets a new password for the specified user.

$ passwd
# Changes the password for the current user.
```

### 15. `systemctl` (System Control)

```bash
$ sudo systemctl start httpd
# Starts the 'httpd' service.

$ sudo systemctl stop httpd
# Stops the 'httpd' service.

$ sudo systemctl enable httpd
# Enables the 'httpd' service to start automatically at boot.
```

### 16. `journalctl` (System Journal)
- **Purpose**: Accesses the system journal, which logs system events.
- **Usage**: `journalctl [options]`
- **Common options**:
  - `-f`: Follow the log output.
  - `-u`: Filter by unit name.
  - `-p`: Filter by priority level.

```bash
$ journalctl -f
# Displays the system journal and follows the log output.

$ journalctl -u httpd
# Displays the journal entries related to the 'httpd' service.
```

### 17. `free` (Free Memory)
- **Purpose**: Displays information about available memory.
- **Usage**: `free [options]`
- **Common options**:
  - `-h`: Human-readable format.

```bash
$ free -h
# Displays memory usage in a human-readable format.
```

### 18. `du` (Disk Usage)
- **Purpose**: Displays disk space usage for files and directories.
- **Usage**: `du [options] file/directory`
- **Common options**:
  - `-h`: Human-readable format.
  - `-a`: Display disk usage for all files.

```bash
$ du -h /home
# Displays disk usage for the '/home' directory in a human-readable format.

$ du -a /home
# Displays disk usage for all files and directories within '/home'.
```

These commands are essential for managing packages, system resources, and user accounts on a Linux system. Practice using them to become proficient in administering your environment.

---

[Previous Page](BasicCommandLineUsage.md)
