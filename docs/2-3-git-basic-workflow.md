# Basic Git Workflow on Local Repo


## Visualizing the Workflow

In this section and the next, you will learn how to make commits in your local repo. Before we go into details, it is helpful to get a bigger picture of the workflow by visualizing a git workflow for collaborative development. Try the following steps on http://git-school.github.io/visualizing-git/

This page is embedded below if you prefer to stay on this page

```
git commit -m "Femur Mesh"
git commit -m "TIbia Mesh"

# Make a new branch from "Femur Mesh" commit to add material properties. Give commit id for "Femur Mesh"
git branch  <branch name> <commit id>
git checkout <branch name>
git commit -m "Femur Properties"
git merge master
```

<iframe src="http://git-school.github.io/visualizing-git/" width="100%" height="700"></iframe>

We used command line for the git actions in the example above. We will supplement GUI (GIt Extensions) illustrations in the rest of the workshop for those not familiar with command line. Most of the git actions can be executed through GUI applications

## The Three Git Areas (States)

The files that are tracked by Git can exist in three states: 

- **modified**
- **staged**: marked to go into your next snapshot (to be committed/saved)
- **committed**: data that is saved to your local repository

The files move between three areas depend on their state (Working Directory, Index, [local] Repository)[^1]:

- You modify the files in the **Working Directory** (also known as Working Tree)
- Files that are ready to committed are moved to **Index** (also know as **Staging Area**) to be get them ready for the snapshot
- Files prepared in the Index are then safely stored in your **local Git repository**  

![Git directory](img/git-directory-translate-illustration.png)

[^1]: 1.3 Getting Started - What is Git?, Pro Git Book, https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F

The basic Git workflow [^2] that we are going explore in this section goes something like this (see the figure below):

- You checkout the project and modify files (in your working directory)
- You selectively stage just those changes you want to be part of your next commit, which adds only those changes to the staging area.
- You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory.

[^2]: Adapted from https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F

![Git directory](img/basic-git-workflow.png)
## What happened when you cloned?

Working tree populated from the index (checkout)

## Stage (git add)

## Commit (git commit)
