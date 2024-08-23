
The command line interface (CLI) is a powerful way to interact with a Linux system. Here are some fundamental commands and concepts to get you started:

**1. Navigating the File System:**

- **`ls`**: Lists files and directories.

  ```bash
  ls           # List all files and directories in the current directory
  ls -l        # Long listing format with detailed information
  ls -a        # Include hidden files
  ```

- **`cd`**: Changes the current directory.
  ```bash
  cd /path/to/directory   # Change to specified directory
  cd ..                   # Move up one directory level
  cd ~                    # Change to the home directory
  cd -                    # Change to the previous directory
  ```

- **`pwd`**: Displays the present working directory.
  ```bash
  pwd   # Print the full path of the current directory
  ```

**2. File Manipulation:**

- **`cp`**: Copies files or directories.
  ```bash
  cp source_file destination_file     # Copy a file
  cp -r source_directory destination_directory   # Copy a directory and its contents
  ```

- **`mv`**: Moves or renames files or directories.
  ```bash
  mv old_name new_name    # Rename a file or directory
  mv file /path/to/destination/   # Move a file to a different directory
  ```

- **`rm`**: Removes files or directories.
  ```bash
  rm file   # Remove a file
  rm -r directory   # Remove a directory and its contents
  rm -i file   # Prompt before each file removal
  ```

- **`mkdir`**: Creates a new directory.
  ```bash
  mkdir new_directory   # Create a new directory
  mkdir -p /path/to/new_directory   # Create parent directories as needed
  ```

- **`rmdir`**: Removes empty directories.
  ```bash
  rmdir directory   # Remove an empty directory
  ```

- **`touch`**: Creates an empty file or updates the timestamp of an existing file.
  ```bash
  touch new_file   # Create an empty file or update the timestamp
  ```

**3. Viewing and Editing Files:**

- **`cat`**: Concatenates and displays file contents.
  ```bash
  cat file   # Display the contents of a file
  ```

- **`less`**: Views file contents one page at a time.
  ```bash
  less file   # View the contents of a file with paging
  ```

- **`more`**: Similar to `less`, but less feature-rich.
  ```bash
  more file   # View the contents of a file with paging
  ```

- **`nano`**: Simple text editor.
  ```bash
  nano file   # Open a file in the nano text editor
  ```

- **`vim`**: Powerful text editor (requires learning basic commands).
  ```bash
  vim file   # Open a file in the vim text editor
  ```

**4. File Permissions and Ownership:** {see [[File Permission]] for more details}

- **`chmod`**: Changes file permissions.
  ```bash
  chmod 755 file   # Set read, write, and execute permissions for owner, and read and execute for group and others
  ```

- **`chown`**: Changes file owner and group.
  ```bash
  chown user:group file   # Change the owner and group of a file
  ```

**5. Process Management:** {see [[Process Management]] for more details}

- **`ps`**: Displays information about running processes.
  ```bash
  ps           # List processes started by the current user
  ps aux       # List all processes with detailed information
  ```

- **`top`**: Displays real-time system resource usage.
  ```bash
  top          # Show an interactive view of running processes and system usage
  ```

- **`kill`**: Terminates a process.
  ```bash
  kill PID     # Terminate a process by its Process ID (PID)
  kill -9 PID  # Forcefully terminate a process
  ```

**6. Network Commands:** [[Networking Basics]]

- **`ping`**: Checks network connectivity.
  ```bash
  ping google.com   # Send ICMP ECHO_REQUEST packets to a network host
  ```

- **`ifconfig`/`ip`**: Configures network interfaces.
  ```bash
  ifconfig           # Display network interface information (older tool)
  ip addr show       # Display network interfaces and addresses (newer tool)
  ```

- **`netstat`**: Displays network connections, routing tables, and interface statistics.
  ```bash
  netstat -tuln   # List all listening ports and their states
  ```

**7. System Information:**

- **`uname`**: Displays system information.
  ```bash
  uname -a   # Show all system information
  ```

- **`df`**: Reports file system disk space usage.
  ```bash
  df -h      # Display disk space usage in human-readable format
  ```

- **`du`**: Estimates file space usage.
  ```bash
  du -sh directory   # Show total disk usage of a directory
  ```

- **`free`**: Displays memory usage.
  ```bash
  free -h    # Show memory usage in human-readable format
  ```

These commands form the foundation of interacting with a Linux system through the command line. Mastery of these basics will enable you to perform essential tasks efficiently and pave the way for learning more advanced command-line skills.

next -> [[User and Group]].

back -> Linux [[File System]].