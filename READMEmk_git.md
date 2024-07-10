# SESSION 1 Learnings 
 ## version control system
   VCS is a system which records   changes done in a file, so that we can recall the versions later. Its important for tracking history of any project we are working on and allowing multiple people to work on the same project at the same time. 

Here are some types of VCS

1.**local version control system**- It keeps track of changes to files on a local system.
Each file is versioned separately, often using a simple database or even individual file copies.

2.**centralized VCS** - These have a single server that stores all versioned files, and clients check out files from this central place.
All version control activities occur through this central server.

3.**Distributed VCS** -It store the entire history of the project on every user's local repository.
Each user has a complete copy of the repository, including all branches and revisions

- **Git as a distributed VCS** -
Git is a distributed version control system,thus every developer has the full record of the projects he has been working on and along with that it provides various advantages like collaboration, faster operations, better data redundancy etc.

###  Git basic concepts
- Repositories 
a repository is a place where the history of our work is stored.
 > Local Repository - these are on the local devices of our machine
 > Remote Repositories - These are hosted by a server and can be accesssed by others.

- Branches- Branches are the parallel version of a repository and these helps developers to make changes in the model or project in some part without making it difficult for the developer to keep track of the whole project.

- Staging Area - A place where we can group changes before we commit them 
- Commit - Its a fundamental unit of change.When we commit, Git takes all the files in the staging area and stores a copy of them in the repo. Thus allowing us to track changes , revert to previous versions, and collaborate with others effectively.

- Tracked and Untracked file 
>Tracked files - These files are in the last commit of the repository.

> Untracked Files - These files are all other files in the working directory and these can be said as the new files.

- States of file in Git 
 > Unmodified - the file which are not changed since the last commit

 > Modified-The file has changed since last commit but changes are not yet staged 

 > staged- The file has been changed and the changes have been added to the staging area, where it is ready to be committed.
 
### Github basic concepts

GitHub is a web-based platform that provides version control using Git and allows for collaboration on software projects.

- VCS platform - GitHub integrates Git, the distributed version control system, providing a web interface for Git repositories.

These are some of the benefits of Github

- Collaborations 
- Hosting services 
- Community 

**Pull, Push and Fork**
- Pull Requests - Helps submitting contributions to a project, along with that allows a developer to propose changes and discuss with collaborators.


- Pushing Changes - Pushing changes in GitHub refers to uploading your local repository changes to a remote repository hosted on GitHub.

- Fork - Forking allows you to create a personal copy of someone else's repository under your GitHub account. This copy acts as an independent version that you can modify without affecting the original repository.


# SESSION 2 Learnings

Here, in session 2 we have dived diper into the installations and setup of git. The mentor started with the basic operations and them moved to advance concepts

### Installing Git 
To intsall git we just have to go to the website and download the same for the corresponding operating system and RAM.



After installation we need to check the version of the git installed and for that we need to open the terminal or command prompt and using :-
**git --version** 
![image](https://github.com/muskank1-2/gitrepo/assets/169113658/8361ff63-2c91-4065-9978-196995b5de73)



### Git Commands

Now before strting with the git commands we have to select the directory in which we want to work.

1. The git init command is used to create a new Git repository. It initializes a new, empty repository in the directory you specify, or in the current directory.

 ```bash
   git init
   ```


2. The git config command is used to configure Git settings.It allows you to set and get configuration variables that control all aspects of how Git looks and operates.

 
3.  Add your name and email using these commands 
    ```bash
        git config user.name"<name>"
        
    git config user.email "<email>"

    ```
4. Using add command we can make changes in the working directory to the staging area. This is the first step in the process of committing changes to the repository.Also the file added is named as *ex1*

``` bash
  git add <file>
 ```

5. Using git commit command records the changes in the local repository, along with a message describing the changes.

``` bash
  git command -m "message"
  ```

  The result of all the 5 commands stated above is shown in the following screenshot :
  
  ![image](https://github.com/muskank1-2/gitrepo/assets/169113658/d0fad47e-8bb0-41a9-a4f1-71a0e9be2b8c)


  we can also make changes in the existing commit message without adding a new message using :- 
  (Here a diff example is used to show how ammend works)
   ```bash 
    git ammend -m " new message"
  ``` 
 ![image](https://github.com/muskank1-2/gitrepo/assets/169113658/c46f9f85-005f-4b19-8698-2a7f928506c5)

  6. Now we will create a branch for our repository using 
  ```bash
  git branch -M main
```
## -- Creating new Repo in Github

 7. Now after this we will have to go to the github web page abd login with the id and password.

 After which we will go to the homepage and create a new repository using *New* button at the right top corner. 
 (created a new repo named "gitrepo")


 ![image](https://github.com/muskank1-2/gitrepo/assets/169113658/e9a0df09-60f4-4e07-b656-f3a360eb3324)


 

 8. After creating the new repo, we have to push the commits using
 ```bash 
 git remote add origin https://github.com/muskank1-2/gitrepo.git
```
## -- Push

9. Now we will send the local commit on the main branch to the remote repository 

```bash 
git push origin main
```
![image](https://github.com/muskank1-2/gitrepo/assets/169113658/d84fc8fe-9e01-42a7-bbd4-3ecc481bd911)



## -- Pull

10. If we have made changes in our git hub repository, we will have to pull the changes as shown 

```bash 
git pull origin main
```

![image](https://github.com/muskank1-2/gitrepo/assets/169113658/9584668f-d4b6-4c65-a231-025f14502a01)


## -- Diffing 
  Diffing in git is used for comparing changes between different states of a repository, such as between commits, branches, the working directory, and the staging area. This comparison helps you see what has changed, where it has changed, and how it has changed. 

  for ex in this assign we have made some changes in the "ex1.txt" file and using the command, we can check the changes as shown in the ss.
  ```bash 
  git diff
  ```

  After this if we want to check whether the file is staged or not we can use the *status* command as shown 
  ```bash 
  git status 
  ```
  As the file was unstaged, we will add the file and move it to staging area.

![image](https://github.com/muskank1-2/gitrepo/assets/169113658/50abc1b7-b959-4024-aa62-322040ce5d24)


Now as the changes were not committed we will commit the changes and check the status 



 ## -- Branches![image](https://github.com/muskank1-2/gitrepo/assets/169113658/a500aae4-1b22-4393-bdc5-b79d4dba1d90)

 Branches in Git are a way to work on different versions of a repository simultaneously.
The defaukt branch in Git is the  main or master branch and we have been working with the "main" branch till now ,

To work with diff branches we will have to follopw the commands in order to create new branches and work with it 

 11. Create a new branch branch1 using :
 
```bash
  git branch branch1
```
we can check how many branches we have using and on what branch we are working  using:

```bash
  git branch 
```

12.In order to switch between branches in Git we use :

```bash
  git checkout <branch>
```
![image](https://github.com/muskank1-2/gitrepo/assets/169113658/6776d29e-20b5-4196-af78-7387f1957f42)


## --Merge and Merge Conflict
There are situations where we have to merge the changes made indifferent branches into one single branch and to do so we use the concept of merging branches in Git.
We have created two txt files with the same name "cpp.c" on different branches, one is on branch1 and other is on main.
Now we will add same content in both the files and try to merge them using 
```bash
  git merge <branch_to_be_merged>
```

The following pictures shows the result:
![image](https://github.com/muskank1-2/gitrepo/assets/169113658/68997f6e-6d74-4b13-95e2-8ab108d78cd2)

## Solving merge conflict 
In order to solve the merge conflict we will first check the stauts and after that we will make changes manually in the "python.py" files.
 13. Open the file in a text editor or IDE as shown :
 
![image](https://github.com/muskank1-2/gitrepo/assets/169113658/0d40a156-a1e5-453e-bd0b-5cfc15321078)


 now remove the "<<<<<<<<"  ,"======" ,">>>>>>>>" signs and then make the changes as per your need.

 14. Add the resolved file using :
 
```bash
  git add python.py

```


15. Commit the changes and check the status to verify the merge 
![image](https://github.com/muskank1-2/gitrepo/assets/169113658/129d0888-efd1-493c-a361-c5a51215f28f)



Thus with all the learning of session 1 and session 2 of git and github I have completed this project
Thankyou HOTWAX System and team for the guidance.

