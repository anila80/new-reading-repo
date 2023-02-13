# Reading-notes-repo- Git Intro

## Table of contents

1. Prerequisities
2. Version control
    - Local Version Control
    - Centralized Version Control
    - Distributed Version Control
3. History of GIT
4. Getting Started
    - Download Git
    - Graphical Clients
    - Initial Customization
    - Default Text Editor
    - Check Settings
    - Getting Help
6. Setting up a GIT Repository
    - Importing
    - Cloning
7. Workflow
    - Local Repository Structure
    - Saving Changes
    - The lifecyle of File Status
    - Check file status
    - Tracking and staging a new file
    - Committing a file
    - Committing all changes
    - Pushing Changes
    - Stashing Changes
 8. Remote Repositories
    - Cloned Repositories
    - Seeing Your Remote
   
   
## Prerequisities
Requires solid understand of Terminal for Mac or Command line for Windows and Linux

## Version control
Version control allows to:
- revisit various versions of a file or set of files
- track modifications
- track modifying individuals
- compare changes
- rectify mistakes

### **Local Version Control**
A local version control system is a local database located on your local hard disk that store changes to files.

### **Centralized Version Control**
A centralized version control system offers software development teams a way to collaborate using central server.

### **Distributed Version Control**
A distributed version control system bring a local copy of the complete repository to every team member, so they can commit, branch and merge locally. 

### So, what is GIT?

**Snapshots**
Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.

**Local Operations**
Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

**Tracking Changes**
Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.

**Loss of Data**
Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

**States**
Files in Git can reside in three main states: committed, modified and staged.

***Committed***

Data is securely stored in a local database

***Modified***

File has been changed but not committed to the database

img src = "https://blog.udemy.com/wp-content/uploads/2015/08/image066.png"

## History of GIT
Git was originally authored by Linus Torvalds in 2005 for development of the linux kernel. 

## Getting Started

### **Download Git**
Git can be installed in 3 ways:
- Install as package
- Install via another installer
- Download and comile the source code

### **Graphical Clients**
Git includes GUI tools, however, users can also utilize third party tools created for particular platforms.

### **Initial Customization**
After installation of Git, you should perform some steps, required once on the computer after installation. To change settings, you can repeat these steps:

- Configuration of variables:
   git config

- identity setting
   git config --global user.name "Anila Khan"
   git config --global user.email "anilarahimkhan@hotmail.com"
 
 To confirm that you have correct settings, use these commands:
 git config --global user.name (it will display the name you entered)
 git config --global user.email (it will display your email address)
-  
**Default Text Editor**
vim is the default text editor, to configure a different text editor used following command in your terminal or command line

$ git config --global core.editor emacs

**Check Settings**
To check settings, use 

Example:

$ git config --list

user.name=Jane Smith

user.email=example@email.com

color.status=auto

color.branch=auto

color.interactive=auto

**Getting Help**

git help command

git command --help

man git-command

## Setting up a GIT Repository

### **Importing**
To import an existing project or directory:

1. swithc to the target project's directory
$ cd test (cd = change directory)

2. use the git init command
$ git init
(At this stage, you have created a new subdirectory named .git that has the repository files. Tracking has not commenced.)

3. To start tracking these repository files, type:
$ git add *.c
$ git add LICENSE
$ git commit -m “any message here”

### **Cloning**
To make a Copy of an existing Git repository

$ git clone URL

## Workflow

### **Local Repository Structure**
The local Git repository has three components:

1. Working Directory: The actual files reside here.
2. Index: The area used for staging
3. Head: Points to the most recent commit

img src ="https://blog.udemy.com/wp-content/uploads/2015/08/image036.png"


### **Saving Changes**
All files in a checked our or working copy of a project file are either in a tracked or untracked state.

1. ***Tracked files***  can be modified, unmodified, or staged; they were part of the most recent file snapshot.

2. ***Untracked files*** were not in the last snapshot and do not currently reside in the staging area.

*After cloning, a repository, files have traced status and are unmodified because they have been checked out but not edited.


## **The lifecyle of File Status**

1. After you edit a file, Git flags it as modified because of changes made after the previous commit.
2. You stage the modified file.
3. Then, you commit staged changes.

img src = "https://blog.udemy.com/wp-content/uploads/2015/08/image006.png"


### **Check file status**

To determine the state of files, utilize the git status command:

$ git status

On branch master

nothing to commit, workig directory clean

*This information indicates which branch you're on (we will cover)*This information indicates which branch you’re on (we will cover branches in a later section) and states “working directory clean,” which means that files have tracked or modified status at the moment. Also, no untracked files are present because Git has not listed any.

## **Tracking and staging a New File**

1. **Single File:**
    Track one file only by using the following format:

    $ git add filename

2. **All Files:**
    Track all files in a repository by using the following command:
    
    $ git add *

After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:

$ git status

On branch master

Changes to be committed:

  (use "git reset HEAD ..." to unstage)
  
new file: EXAMPLE
  

## **Committing a File**

After staging one or multiple files, you should commit the changes adn record what you did within the commit message:

$ git commit -m “made change x,y,z”

*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.


## **Committing All Changes**

$ git commit -a

## **Pushing Changes**

Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.

Example:

$ git push origin master

## **Stashing Changes**

When you are not ready to commit changes but do not want to lose them either, git stash is a great option. This command temporarily removes changes and hides them, giving you a clean working directory. When you are ready to continue working on the changes, simply use the git stash apply command to retrieve the hidden changes.


## **Remote Repositories**

In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.

### **Cloned Repositories**
As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.

### **Seeing Your Remote**
By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.

By using git remote -v, you can view all the remote URLs next to their corresponding short names.

$ cd example

$ git remote -v

remote1 https://github.com/remote1/example (fetch)

remote1 https://github.com/remote1/example (push)

remote2 https://github.com/remote2/example (fetch)

remote2 https://github.com/remote2/example (push)

remote3 https://github.com/remote3/example (fetch)

remote3 https://github.com/remote3/example (push)

### **Adding Remotes**

To create a new remote Git repository with a short name, use the following format:

git remote add shortname url

Example:

$ git remote

origin

$ git remote add js https://github.com/janesmith/project1

$ git remote -v

origin https://github.com/johndoe/project1 (fetch)

origin https://github.com/johndoe/project1 (push)

js     https://github.com/janesmith/project1 (fetch)

js     https://github.com/janesmith/project1 (push)
This addition of these remote and short names allows you to use shortnames for Git collaboration.

### **Fetching**

Fetching entails pulling data that you don’t have from a remote project.

Here is the command format:

git fetch [remote-name]

*Now, you should also possess the references to all branches for that remote (more on branching later).

Cloned Repositories

For cloned repositories, use the command git fetch origin to pull down any new changes that were pushed to the server since you cloned or last fetched from it.

Note: git fetch solely pulls new data to a local repository; it does not merge changes with or modify your local work. We will discuss merging in a later section. Later, we will also discuss git pull , which allows for fetching and automatic merging.

### ***Pushing***

To push your changes “upstream” for sharing, you would use the following git push command format:

git push [remote-name][branch-name]
Example:

$ git push origin master
*This command pushes committed changes from your local “master” branch upstream to the “origin” server.

Note: You can only successfully push changes upstream if you have write access for the server from which you cloned, and if someone else has not pushed changes upstream that you haven’t pulled yet. If a collaborator pushed changes upstream after you had cloned, your push will not be successful. You will have to pull new changes and merge them with your branch before you can successfully push your changes upstream.

### **Renaming/Removing Remotes**

***Rename***

To rename a remote’s short name, use the git remote rename command.

Example:

$ git remote rename js jane

$ git remote

origin

jane
*In the example above, we can see that the remote’s short name has been changed from js to Jane. The command git remote lists our existing remotes, which jane is now one of. The rename action also alters names of remote branches: js/master would change to jane/master.

***Remove***

To remove a remote for whatever reason (e.g., a contributor has left the team, the server has moved), simply use the git remote rm command:

Example:

$ git remote rm jane

$ git remote

origin
NOTE: Reminder: “origin” is simply the default remote name when you use the git clone command.

## **Undoing Actions**

Git has mechanisms for undoing certain actions.

### Commit Mistakes

You can use the –amend command when you need to alter a commit message or forgot to add some files.

$ git commit --amend
In the example above, you can use this command to easily change your commit message, if no changes were made since the newest commit.

$ git commit -m “my first commit”

$ git add example_file

$ git commit --amend
In the above example, a forgotten file is added to a commit.

### Unstaging a File

$ git reset HEAD index.html

Unstaged changes after reset:

M index.html
Above, we see that the git reset HEAD command unstaged the index.html file.

NOTE: When git reset --hard is used, Git overwrites all changes in the working directory, permanently destroying any uncommitted changes.

### Undo a Committed Snapshot

To undo changes resulting from a particular commit, use the git revert command. This command appends a new commit that undoes changes introduced by a specific commit. This prevents Git from losing history.

$ git commit -m "Example Commit"

$ git revert HEAD
*In the example above, a new commit gets appended and rolls back changes from a specific commit.

### Unmodifying a File

To have a file return to its state when you last committed, utilize the git checkout command.

Example:

$ git checkout -- index.html

