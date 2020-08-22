# **Basic Git Workflow on Local Repo**

## **Getting an Intuition**

In this section and the next, you will learn how to make commits in your local repo and make them available on the remote repo. Before we go into details, it is helpful to get an overview of the git workflow by visualizing a git workflow for collaborative development. 

Try the following steps one by one on http://git-school.github.io/visualizing-git/ _(This page is embedded below if you prefer to stay on this page. Trying refreshing if you see a blank embedded window)_

```
git commit -m "Femur Mesh"
git commit -m "TIbia Mesh"

# Make a new branch from "Femur Mesh" commit to add material properties. Give commit id for "Femur Mesh"
git branch  <branch name> <commit id>
git checkout <branch name>
git commit -m "Femur Properties"
git merge master
git checkout master
```

<iframe src="http://git-school.github.io/visualizing-git/" width="100%" height="700"></iframe>

From the illustration above, note:

- how commits are made as updates are made to a repo
- how a branch was created to work in parallel and merge the updates into the ``master`` branch. 
- the `HEAD` moved as you switched between the branches. `HEAD` indicates the branch where the next commit will be written on. (Think of it like the _'recording head'_ that writes on a gramophone record or CD/DVD)

<!---
!!! tip "Git GUI Client" 
        
    We used command line for the git actions in the example above. We will also be showing you how to do these actionsi using Git GUI Client (Git Extensions).
-->

## **The Three Git Areas (States)**

The files that are tracked for changes by Git can exist in three states: 

- **modified**
- **staged**: marked to go into your next snapshot (to be committed/saved)
- **committed**: data that is saved to your local repository

The files move between **_three areas_** depending on the state (Working Directory, Index, [local] Repository)[^1]:

- You _modify_ the files in the **Working Directory** (also known as Working Tree)
- Files that are ready to committed are moved to **Index** (also know as **Staging Area**) to be get them _ready for the snapshot_
- Files prepared in the Index are then safely _committed_ in your **local Git repository**  

![Git directory](img/git-directory-translate-illustration.png)

[^1]: 1.3 Getting Started - What is Git?, Pro Git Book, https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F

The basic Git workflow [^2] that we are going explore in this section goes something like this (see the figure below):

1. You checkout the project and modify files (in your working directory)
2. You selectively stage just those changes you want to be part of your next commit, which adds only those changes to the staging area.
3. You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory.

[^2]: Adapted from https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F

![Git directory](img/basic-git-workflow.png#center){: style="width:550px"}

## **Hands-on Exercise**

### **1. Clone the exercise repo**

(Skip this step if you did this already in the pre-workshop setup)

Go to the directory where you would like to clone your repo and use the clone command. On Windows, you can easily open the Git Bash using right click in your prefered directory

```
git clone git@virtual.openvt.eu:viva-workshops/intro-exercise.git
```

Alternatively on GUI

![](img/Git-extension-main-options.png#center){: style="width:400px"}

Use the address for SSH cloning in the Clone window 

![Git Extensions Clone](img/Git-extensions-Clone-Window.png)

This step creates from the remote repo (on OpenVT) and checkout out the latest version to populate your working directory/tree

Enter the repo and check the files in the repo

```
cd intro-exercise
```
You will be able to see a `README.md` and the hidden `.git` folder

### **2. Make a branch and switch to the new branch**

git checkout -b FirstName-LastName

If you arleady created a branch during the pre-workshop setup, then switch to your branch using the following command.

```
git checkout FirstName-LastName
```


### **3. Make changes to the repo and save them**

As an exercise, we will be collaboratively creating a list of the workshop participants

In this step, we will make changes to the repo and stage the updated files to Index for committing them. 

#### a. Create a new file in the repo

Add a new markdown file `FirstName-LastName.md` to the directory. Open the file and leave a message.

#### b. Check the status of your repo
Check the status of your repo

```
git status
```

You can see that the new file is shown as untracked

On Git Extensions, the green `+` sign indicates that there are new files that are not tracked

![](img/GIt-extensions-git-status.png#center){: style="width:500px"}
 

#### c. Stage

The first step to store your new file or update a modified file is to stage it (to move it to the index/staging area). `git add` is the command for this action

```
git add FirstName-LastName
```

![git add](img/git-add.png#center){: style="width:350px"}

If you `git status` again, you will find that this file has been staged to be committed.

#### d. Commit

Now you are ready to make the commit(save) to your Git repository (Doing `git status` again will shown that these files are staged(or are currently in the index region))

You need to provide a commit message as you make the commit. The easy way to do this is to give a one line commit message with the `git commit` command

```
git commit -m "Add FirstName to Repo"
```

![Git commit](img/git-commit.png#center){: style="width:350px"}

If you again do `git status` now, you will see that the working tree is clean and everything has been committed

!!! example "Breakout Room Task: Edit the README"
    
    We are collaboratively list the participants in the README.md files. In this step, you will add your name to the README file and link the text file you created in the previous step.   

    1. Edit the README.md to add your name to the list of workshop participants.
    2. Link you name on the README to the file you created using the markdown syntax for linking `[Text to link](Link)`:
         ```
         [FirstName LastName](FirstName-LastName.md)
         ```
    3. Check the status using `git status`
    4. Stage and commit the README file with a commit message.
        ```
        git add README.md
        git commit -m "Add FirstName to Participant list"
        ```


