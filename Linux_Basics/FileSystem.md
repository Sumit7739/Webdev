### Linux File System


The Linux file system is a structured and organized way of storing and managing files on a Linux operating system. It follows a hierarchical directory structure, with the root directory (`/`) at the top. Here’s a brief overview of key components and concepts:


**1. Hierarchical Directory Structure:**


- **Root Directory (`/`)**: The top level of the file system from which all other directories branch out.


**2. Important Directories:**


- **`/bin`**: Contains essential user command binaries (executables) needed for booting and repairing the system.

- **`/boot`**: Stores files needed to boot the system, including the kernel and initial ramdisk images.

- **`/dev`**: Contains device files that represent hardware components (e.g., hard drives, printers).

- **`/etc`**: Houses configuration files for the system and applications.

- **`/home`**: Contains personal directories for each user. For example, a user named `john` would have `/home/john`.

- **`/lib`**: Includes shared library files required by binaries in `/bin` and `/sbin`.

- **`/media`**: Used for mounting removable media like CDs, DVDs, and USB drives.

- **`/mnt`**: Commonly used for temporarily mounting file systems.

- **`/opt`**: Contains add-on application software packages.

- **`/proc`**: A virtual filesystem that provides process and system information from the kernel.

- **`/root`**: The home directory for the root user (system administrator).

- **`/sbin`**: Holds system binaries essential for system administration.

- **`/srv`**: Contains data for services provided by the system (e.g., web servers).

- **`/tmp`**: Used for temporary files; often cleared on reboot.

- **`/usr`**: Contains user applications and utilities. It has subdirectories like `/usr/bin` (user binaries), `/usr/lib` (libraries), and `/usr/share` (shared data).

- **`/var`**: Stores variable


 **3. File Types:**

- **Regular Files**: Standard files containing data, text, or executable code.

- **Directories**: Containers that hold other files and directories.

- **Device Files**: Represent hardware devices (block devices for storage, character devices for serial devices).

- **Symbolic Links**: Pointers to other files or directories.

- **Pipes**: Used for inter-process communication.

- **Sockets**: Enable communication between processes or over networks.


**4. File Permissions:**  *{see [[Read,Write and Execute]] page for more details}*


- **Read (`r`)**: Permission to read the contents of a file or directory.

- **Write (`w`)**: Permission to modify a file or directory.

- **Execute (`x`)**: Permission to execute a file or traverse a directory.data like logs, databases, and email.


NEXT -> [Basic Command Line Usage](BasicCommandLineUsage.md).

BACK -> [History](History.md).
