
**Highlights of the Topics:**  

1. **Introduction to Git**
2. Git Repository Structure
3. Github
4. Accessing Github central repository via HTTPS or ssh
5. Working with git – Important Git commands

### **Introduction to Git**

Git is a distributed version control system. So, **What is a Version Control System?** 

A version Control system is a system that maintains different versions of your project when we work in a team or as an individual. (system managing changes to files) As the project progresses, new features get added to it. So, a version control system maintains all the different versions of your project for you and you can roll back to any version you want without causing any trouble to you for maintaining different versions by giving names to it like MyProject, MyProjectWithFeature1, etc. 

Distributed Version control system means every collaborator(any developer working on a team project)has a local repository of the project in his/her local machine unlike central where team members should have an internet connection to every time update their work to the main central repository. 

So, by distributed we mean: the project is distributed. A repository is an area that keeps all your project files, images, etc. In terms of Github: different versions of projects correspond to commits.

---


### **Git Repository Structure**

It consists of 4 parts:  

1. **Working directory:** This is your local directory where you make the project (write code) and make changes to it.
2. **Staging Area (or index):** this is an area where you first need to put your project before committing. This is used for code review by other team members.
3. **Local Repository:** this is your local repository where you commit changes to the project before pushing them to the central repository on Github. This is what is provided by the distributed version control system. This corresponds to the .git folder in our directory.
4. **Central Repository:** This is the main project on the central server, a copy of which is with every team member as a local repository.


All the repository structure is internal to Git and is transparent to the developer. 

**Some commands which relate to repository structure:**  

 ```bash

git add . # transfers your project from working directory to staging area.

git commit -m "your message here" ->
# transfers your project from staging area to Local Repository.

git push
# transfers project from local to central repository.(requires internet)

  ```


### **Github**

Github basically is a for-profit company owned by Microsoft, which hosts Git repositories online. It helps users share their git repository online, with other users, or access it remotely. You can also host a public repository for free on Github. 

User share their repository online for various reasons including but not limited to project deployment, project sharing, open source contribution, helping out the community and many such.

### **Accessing** Github **central repository via HTTPS or SSH**

Here, transfer project means transfer changes as git is very lightweight and works on changes in a project. It internally does the transfer by using Lossless Compression Techniques and transferring compressed files. Https is the default way to access Github central repository.  

- **By git remote add origin http_url:** remote means the remote central repository. Origin corresponds to your central repository which you need to define (hereby giving HTTPS URL) in order to push changes to Github.
- **Via SSH:** connect to Linux or other servers remotely.

If you access Github by ssh you don’t need to type your username and password every time you push changes to GitHub.

**Terminal commands:**

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
This does the ssh key generation using RSA cryptographic algorithm.

eval "$(ssh-agent -s)" -> enable information about local login session.

ssh-add ~/.ssh/id_rsa -> add to ssh key.
cat ~/.ssh/id_rsa (use .pub file if not able to connect)
add this ssh key to github.


Now, go to github settings -> new ssh key -> create key

ssh -T git@github.com -> activate ssh key (test connection)

Refresh your github Page.
```

### **Working with git – Important Git commands**

**Git user configuration (First Step)**  

```bash
git --version (to check git version)
git config --global user.name "your name here"
git config --global user.email "your email here"
```

These are the information attached to commits.

NEXT -> [Working with Git](GitCMD.md).
