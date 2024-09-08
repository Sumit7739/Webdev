### **Working with git – Important Git commands**

**Git user configuration (First Step)**

```bash
git --version (to check git version)
git config --global user.name "your name here"
git config --global user.email "your email here"
```

**Initialize directory** 
```bash
git init
```

initializes your directory to work with git and makes a local repository. .git folder is made (OR)
```bash
git clone http_url
```

This is done if we have an existing git repository and we want to copy its content to a new place.

**Connecting to the remote** **repository**

```bash
git remote add origin http_url/ssh_url
```

connect to the central repo to push/pull. pull means adopting the changes on the remote repository to your local repository. push merges the changes from your local repository to the remote repository.

```bash
git pull origin master
```

One should always first pull contents from the central repo before pushing so that you are updated with other team members’ work. It helps prevent merge conflicts. Here, master means the master branch (in Git).

**Stash Area in git**

- git stash

Whichever files are present in the staging area, it will move that files to stash before committing it. 

- git stash pop

Whenever we want files for commit from stash we should use this command.

- git stash clear

By doing this, all files from stash area is been deleted.


**Steps to add a file to a remote Repository:** 

First, your file is in your working directory, Move it to the staging area by typing:  

```bash
git add -A (for all files and folders)
#To add all files only in the current directory
git add .
```


**git status:** here, untracked files mean files that you haven’t added to the staging area. Changes are not staged for commit means you have staged the file earlier than you have made changes in that files in your working directory and the changes need to be staged once more. Changes ready to be committed: these are files that have been committed and are ready to be pushed to the central repository.

```bash
git status

git commit -a -m "message for commit"
-a: commit all files and for files that have been
     staged earlier need not to be git add once more
-a option does that automatically.

git push origin master -> pushes your files to
                         github master branch
git push origin anyOtherBranch -> pushes any
                      other branch to github.
git log ; to see all your commits

git checkout commitObject(first 8 bits) file.txt->
revert back to this previous commit for file file.txt
```

Previous commits might be seen through the git log command.

```bash
HEAD -> pointer to our latest commit.
```

**Ignoring files while committing**

In many cases, the project creates a lot of logs and other irrelevant files which are to be ignored. So to ignore those files, we have to put their names in **gitignore** file.

```bash
touch .gitignore
echo "filename.ext" >>.gitignore
#to ignore all files with .log extension
echo "*.log" > .gitignore
```

Now the filenames written in the .gitignore file would be ignored while pushing a new commit. To get the changes between commits, commit, and working tree.

```
git diff
```

The ‘git diff’ command compares the staging area with the working directory and tells us the changes made. It compares the earlier information as well as the current modified information.

**Branching in Git**

```bash
create branch ->
git branch myBranch
or
git checkout -b myBranch -> make and switch to the
                                  branch myBranch

#Do the work in your branch. Then,

git checkout master ; to switch back to master branch

#Now,  merge contents with your myBranch By:

git merge myBranch (writing in master branch)

#This merger makes a new commit.
```

**Another way**

```bash
git rebase myBranch

#This merges the branch with the master in a serial fashion.
Now,  

git push origin master

#To remove  or delete a file 
------------------------------------------------

#To remove.  a file from the  Git repository we use 

git rm “file name”

#To remove only from the staging area 

git rm –cached “ file name”
```

**Undoing change**

To change all the  files to as same as the previous commit then use

```bash
git checkout -f
```

### Contributing to Open Source

Open Source might be considered as a way where user across the globe may share their opinions, customizations or work together to solve an issue or to complete the desired project together. Many companies host there repositories online on Github to allow access to developers to make changes to their product. Some companies(not necessarily all) rewards their contributors in different ways.

---
	