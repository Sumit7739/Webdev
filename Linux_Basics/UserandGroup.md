### From here Intermediate Linux Topics Starts.

### User and Group Management

#### Creating and Managing Users and Groups

1. **Creating Users:**
  
   - **`useradd`**: Command to create a new user.
   
     ```bash
     useradd username      # Creates a new user without a home directory
     useradd -m username   # Creates a new user with a home directory at /home/username
     ```
   
   - **Options:**
     
	 - `-m`: Creates the user's home directory if it does not exist.
     - `-s /bin/bash`: Specifies the default shell for the user.
     - `-c "User Name"`: Adds a comment (usually the full name of the user).


2. **Setting Passwords:**
   
   - **`passwd`**: Command to set or change a user's password.
   
     ```bash
     passwd username       # Prompts to set a new password for the user
     passwd                # Changes the password of the current user if run without a username
     ```

3. **Creating Groups:**
   
   - **`groupadd`**: Command to create a new group.
   
     ```bash
     groupadd groupname    # Creates a new group
     ```
   
   - **Options:**
   
	 - `-g GID`: Specifies the group ID for the new group.


4. **Modifying Users and Groups:**
   
   - **`usermod`**: Command to modify user attributes.

	 ```bash
     usermod -aG groupname username   # Adds the user to an additional group
     usermod -l newname oldname       # Changes the username
     ```
   
   - **Options:**
     
	 - `-aG`: Adds the user to the specified group(s) without removing them from other groups.
     - `-l`: Changes the user's login name.

   - **`groupmod`**: Command to modify group attributes.
     ```bash
     groupmod -n newgroup oldgroup    # Changes the group name
     ```

5. **Deleting Users and Groups:**
   - **`userdel`**: Command to delete a user.
     ```bash
     userdel username       # Deletes the user account
     userdel -r username    # Deletes the user account and the home directory
     ```
   - **`groupdel`**: Command to delete a group.
     ```bash
     groupdel groupname     # Deletes the group
     ```


---


Go back to topics page [[Linux Basics]].