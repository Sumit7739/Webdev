# Git Configuration and Commands

**Basics to Advance Git commands is listed here, practicing them will make working with GIT easier and faster.**

---

### Checking Git Configuration

#### List All Configurations
To view all Git configuration settings, use the following command:
```bash
git config --list
```
This will display all the configuration settings, including local, global, and system configurations.

#### Show Specific Configuration
To check a specific configuration setting, use:
```bash
git config user.name
```
This command will output the currently configured username.

#### Show Configuration Scope
You can use the `--show-origin` or `--show-scope` options to see where each setting is defined:
```bash
git config --list --show-origin
git config --list --show-scope
```
These commands will show the names and values of Git config properties along with their file locations.

---

### Setting Up Git Configuration

#### Setting Up Git Username
To configure your Git username, use:
```bash
git config --global user.name "Your Name"
```
This sets the username globally for all repositories used by the current user.

#### Setting Up Git User Email
To configure your Git email, use:
```bash
git config --global user.email "your.email@example.com"
```
This sets the email address globally for all repositories used by the current user.

#### Caching Login Credentials
To store login credentials in the cache, use:
```bash
git config --global credential.helper cache
```
This command sets up the credential helper to cache your login credentials for a limited time.

---

### Initializing a Git Repository

To start a new Git repository, use:
```bash
git init
```
This command initializes a new Git repository in the current directory.

---

### Adding Files to the Staging Area

**Add a File to the Staging Area**

To add a specific file to the staging area, use:
```bash
git add filename_here
```
Replace `filename_here` with the name of the file you want to add.

#### Add All Files to the Staging Area
To add all files in the current directory to the staging area, use:
```bash
git add .
```
This command stages all files in the project directory.

#### Add Specific Files to the Staging Area
To add files matching a pattern, use:
```bash
git add fil*
```
This command adds all files starting with `fil` to the staging area.

---

### Committing Changes

#### Commit Changes with a Message
To commit changes with a message, use:
```bash
git commit -m "Your commit message here"
```
This command commits the staged changes with a short commit message.

#### Commit Changes and Skip the Staging Area
To add and commit tracked files in one step, use:
```bash
git commit -a -m "Your commit message here"
```
This command adds and commits tracked files without needing to stage them separately.

---

### Viewing Repository Status and History

#### Check Repository Status
To see the status of the current repository, including staged, unstaged, and untracked files, use:
```bash
git status
```
This command provides an overview of the repository's current state.

#### View Commit History
To view the commit history, use:
```bash
git log
```
This command displays a list of commits made to the repository.

#### View Commit History with Changes
To see the commit history including the changes made in each commit, use:
```bash
git log -p
```
This command shows the commit history along with the diff of each commit.

#### View a Specific Commit
To view details of a specific commit, use:
```bash
git show commit-id
```
Replace `commit-id` with the ID of the commit you want to view.

#### View Log Stats
To see commit history with statistics about the changes in each commit, use:
```bash
git log --stat
```
This command displays the commit history along with line and file changes.

---

### Comparing Changes

#### View Unstaged Changes
To see unstaged changes, use:
```bash
git diff
```
This command shows the differences between the working directory and the staging area.

#### View Staged Changes
To see staged changes, use:
```bash
git diff --staged
```
This command shows the differences between the staging area and the last commit.

#### Interactive Staging
To interactively stage changes, use:
```bash
git add -p
```
This command opens a prompt to selectively stage changes.

---

### Managing Files and Branches

#### Remove Tracked Files
To remove a tracked file from the working tree, use:
```bash
git rm filename
```
This command removes the file and stages the removal.

#### Rename Files
To rename a file and stage the change, use:
```bash
git mv oldfile newfile
```
This command renames the file and stages the change.

#### Ignore Files
To ignore files, create a `.gitignore` file and commit it:
```bash
echo "filename" > .gitignore
git add .gitignore
git commit -m "Add .gitignore"
```
This process tells Git to ignore the specified files.

#### Revert Unstaged Changes
To revert changes to a file in the working directory, use:
```bash
git checkout filename
```
This command reverts the file to its state in the last commit.

#### Revert Staged Changes
To unstage changes, use:
```bash
git reset HEAD filename
```
This command unstages the file but keeps the changes in the working directory.

---

### Commit Amendments and Rollbacks

#### Amend the Most Recent Commit
To modify the most recent commit, use:
```bash
git commit --amend
```
This command allows you to modify and add changes to the most recent commit.

#### Rollback the Last Commit
To revert the last commit, use:
```bash
git revert HEAD
```
This command creates a new commit that is the opposite of the last commit.

---

### Branch Management

#### Create a New Branch
To create a new branch, use:
```bash
git branch branch_name
```
This command creates a new branch but does not switch to it.

#### Switch to a Branch
To switch to a branch, use:
```bash
git checkout branch_name
```
This command switches to the specified branch.

#### Create and Switch to a New Branch
To create and switch to a new branch in one step, use:
```bash
git checkout -b branch_name
```
This command creates a new branch and switches to it immediately.

#### List Branches
To list all branches, use:
```bash
git branch
```
This command displays all branches and highlights the current branch.

#### Delete a Branch
To delete a branch, use:
```bash
git branch -d branch_name
```
This command deletes the specified branch if it has been fully merged into the current branch.

---

### Merging and Rebasing

#### Merge Two Branches
To merge the history of one branch into another, use:
```bash
git merge branch_name
```
This command merges the specified branch into the current branch.

#### Show Commit Log as a Graph
To view the commit log as a graph, use:
```bash
git log --graph --oneline
```
This command displays the commit history in a graphical format.

#### Show Commit Log as a Graph for All Branches
To view the commit log as a graph for all branches, use:
```bash
git log --graph --oneline --all
```
This command displays the commit history for all branches in a graphical format.

#### Abort a Conflicting Merge
To abort a merge and return to the state before the merge, use:
```bash
git merge --abort
```
This command throws away the current merge and resets the repository to its state before the merge attempt.

---

### Remote Repositories

#### Add a Remote Repository
To add a remote repository, use:
```bash
git remote add origin https://repo_here.git
```
Replace `https://repo_here.git` with the URL of your remote repository.

#### View Remote URLs
To see the URLs of remote repositories, use:
```bash
git remote -v
```
This command displays the URLs of all remote repositories associated with the local repository.

#### Get More Info About a Remote Repository
To get more information about a remote repository, use:
```bash
git remote show origin
```
Replace `origin` with the name of the remote repository you want to query.

#### Push Changes to a Remote Repository
To push changes to a remote repository, use:
```bash
git push
```
This command pushes the local commits to the remote repository.

#### Pull Changes from a Remote Repository
To fetch and merge changes from a remote repository, use:
```bash
git pull
```
This command retrieves the latest changes from the remote repository and merges them into the local branch.

#### Fetch Remote Repository Changes
To download changes from a remote repository without merging them, use:
```bash
git fetch
```
This command updates the remote tracking branches but does not merge the changes into the local branch.

#### Check Remote Branches
To list the name of all remote branches that Git is tracking, use:
```bash
git branch -r
```
This command displays the names of all remote branches.

#### Merge Remote Repository with Local
To merge changes from a remote repository into the local branch, use:
```bash
git merge origin/main
```
Replace `origin/main` with the name of the remote branch you want to merge.

#### Update Remote Without Merging
To update the remote tracking branches without merging any content into the local branches, use:
```bash
git remote update
```
This command updates the remote tracking branches but does not perform a merge.

#### Push a New Branch to a Remote Repository
To push a new branch to a remote repository, use:
```bash
git push -u origin branch_name
```
This command creates the branch on the remote repository and sets the local branch to track the remote branch.

#### Remove a Remote Branch
To remove a branch from a remote repository, use:
```bash
git push --delete origin branch_name_here
```
This command deletes the specified branch on the remote repository.

---

### Rebasing

#### Rebase Branch
To transfer completed work from one branch to another, use:
```bash
git rebase branch_name_here
```
This command rebases the current branch onto the specified branch.

#### Interactive Rebase
To run an interactive rebase, use:
```bash
git rebase -i master
```
This command opens the editor with a list of commits to interactively rebase.

---

### Forcing a Push Request

#### Force Push Request
To force a push request, use:
```bash
git push -f
```
**Note:** This command is generally not recommended for public repositories as it can overwrite changes made by others.

---

### Git Configuration Levels and Files

#### Local Configuration
- **Scope:** Applies only to a specific repository.
- **Location:** `.git/config` within the repository's directory.
- **Example:** `git config --local core.editor vim`.

#### Global Configuration
- **Scope:** Applies to all repositories used by the current user.
- **Location:** `~/.gitconfig` on Unix-like systems, `C:\Users\USERNAME\.gitconfig` on Windows.
- **Example:** `git config --global user.name "Your Name"`.

#### System Configuration
- **Scope:** Applies across all users on the current machine.
- **Location:** `/etc/gitconfig` on Unix-like systems, `C:\ProgramData\Git\config` on Windows.
- **Example:** `sudo git config --system core.autocrlf false`.

---

### Editing Configuration Files Directly

You can edit configuration files directly using the `--edit` option:
```bash
git config --edit
git config --local --edit
git config --global --edit
git config --system --edit
```
This opens the configuration file in your default editor.

---

back -> [Git basics Commands](GitCMD.md)
