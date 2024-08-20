### Understanding Read, Write, and Execute Permissions

**1. Basic Permissions:**

- **Read (`r`)**: Allows viewing the content of a file or listing the contents of a directory.
  - **File**: `cat file` displays content.
  - **Directory**: `ls directory` lists files.

- **Write (`w`)**: Allows modifying the content of a file or adding/removing files in a directory.
  - **File**: `echo "text" > file` writes to the file.
  - **Directory**: `touch newfile` adds a new file.

- **Execute (`x`)**: Allows running a file as a program or accessing a directory.
  - **File**: `./script.sh` executes a script.
  - **Directory**: `cd directory` changes into the directory.

**Permission Representation:**

- **File Permissions**: Shown as `-rwxr-xr--`
  - `rwx`: Owner permissions
  - `r-x`: Group permissions
  - `r--`: Others permissions

**Numeric Mode:**

- **Example**: `755` represents `rwxr-xr-x`.

### Special Permissions

**1. Setuid (`s`):**

- **Usage**: Executes a file with the privileges of the file owner.
- **Set with**: `chmod u+s file`
- **Example**: `-rwsr-xr-x` (Setuid bit set)

**2. Setgid (`s`):**

- **Usage**: Executes a file with the group’s privileges or sets group ownership on new files in a directory.
- **Set with**: `chmod g+s directory`
- **Example**: `-rwxr-sr-x` (Setgid bit set)

**3. Sticky Bit (`t`):**

- **Usage**: Ensures only the file owner can delete or rename their files in a directory.
- **Set with**: `chmod +t directory`
- **Example**: `drwxrwxrwt` (Sticky bit set)

These commands control who can read, write, or execute files and directories, and set special access rules.

Go back to topics page [[Linux Basics]].