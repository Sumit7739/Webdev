#### File Permissions and Ownership

1. **File Permissions:**

   - **`chmod`**: Changes the permissions of a file or directory.
   
     ```bash
     chmod 755 file       # Owner: read/write/execute, Group: read/execute, Others: read/execute
     chmod u+rwx,go+rx file  # Alternative symbolic notation
     ```
   
   - **Permission Types:**
     - **r (read)**: Permission to read the file or directory.
     - **w (write)**: Permission to modify the file or directory.
     - **x (execute)**: Permission to execute the file or traverse the directory.

2. **File Ownership:**

- **`chown`**: Changes the ownership of a file or directory.

	 ```bash
     chown user:group file     # Change owner and group
     chown user file           # Change only the owner
     chown :group file         # Change only the group
     ```
   
   - **`chgrp`**: Changes the group ownership of a file or directory.
   
     ```bash
     chgrp groupname file      # Change group ownership
     ```

By managing users, groups, and file permissions, you can control access to resources and maintain security within a Linux system.


Go back to topics page [[Linux Basics]].