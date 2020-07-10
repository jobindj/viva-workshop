# **Introduction to Git**

!!! summary "Overview" 

    **Questions**

    - Why version control?
    - Why git?
    - How are files version controled in git?
  
    **Objectives** 
  
    - Learn what is automated version control
    - Aprreciate the need for version control
    - Understand git repository structure
   

Git is an **automated _version control_ system**. 

What is _version control_? "Version control is a system that records the changes to a file or a set of files over time so that you can recall specific versions later."[^1]

[^1]: Pro Git book, https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control

## **Why Version Control?**

!!! Warning "Working in a Team"

    Imagine if 5 co-authors worked on a paper together using 'Track changes'. Either they have to work sequentially (slowing down the process) or they would have to manually merge their contributions. Also, even with track changes, you lose the history once the changes are accepted. 
     
    -   _“I will just finish my work and then you can start with your changes.”_
    -   _“Can you please send me the latest version?”_
    -   _“Where is the latest version?”_
    -   _“Which version are you using?”_

    How cumbersome!

[![PhD Comics](/img/phd-comic-VC.gif#center)](http://phdcomics.com/comics/archive.php?comicid=1531)
    
Here are some of the reasons we need version control, especially in an open source collaborative workflow.

##### Branching

- Work in parallel or on different features

##### Colloboration

- Avoid accidentally overwriting or overlooking someone else's changes/updates. Good conflict management.

##### Roll-back functionality 

- Mistakes happen!
- Nothing commited to version control is ever lost
- Record of changes made: who and when. Makes it easy to track and go to previous version if needed
  
### What can be version controlled?

- Everything that needs to be shared
- anything that changes overtime
- papers, books, datasets.

And now Human Body Finite Element Models!

## **Why git?** 

- Most popular and widely used version control system
- Easy to setup - no server needed
- Efficient and distributed version control (no single point of failure, you can track and clean-up changes offline, simplifies collaboration model for open-source projects.)
- Important platforms such as [GitHub](https://github.com), [GitLab](https://gitlab.com), and [Bitbucket](https://bitbucket.org) build on top of Git.

_(This list is an abridged version from CodeRefinery's Introduction to Git[^2])_
[^2]: https://coderefinery.github.io/git-intro/01-motivation/#why-git

## **Git Basics**

- Git tracks the content of a folder and tracks the changes over time as _snapshots_.
- When a change is ready to be saved, a snapshot of the folder is saved.
  - In the Git world, save is known as **commit**
- These commits are kept in a sub-folder called `.git`
- `.git` contains the whole repository/database (versions, history, ...)
- You can interact with Git through mulitple interfaces: command line, graphical user interface, web interface.

![repo](/img/repo_vivaplus.png#center){: style="width:350px"}

Every time a change in the folder is committed, a new **Commit** is created: _Commit 1, Commit 2, Commit 3, ..._

- Git does not create a copy of unchanged files (optimizes storage)

- Every commit is a full **snapshot** of the whole folder

![snapshots](/img/snapshots.png)

Each commit is connected to its parent: points to its parent as shown below (the files in the snapshots are not shown)

![commit-parent](/img/commit-parent.png)

Commit structure

Commit hash, SHA

## **Git Repo**

A repository (**Repo**) for Git version control is created in two ways:

1. Enable version control on an existing folder
    - `git init`
2. Get a copy of an existing git Repo
    - `git clone`

!!! check "Hands-on Activity: **Clone the VIVA+ repo**" 
    
    URL: https://virtual.openvt.eu/viva/vivaplus

    - Explore the VIVA+ repo. Along with the average female (50F) model and associated subfolders, you can find the `.git` subfolder.

## Some examples from the world of Biomechanics

- [OpenSim](https://github.com/opensim-org/opensim-core)
- [Muscle parameter optimizer](https://github.com/modenaxe/MuscleParamOptimizer)
- [FEBio](https://github.com/febiosoftware/FEBio)
- [GIBBON](https://github.com/gibbonCode/GIBBON)
- 

## Summary

!!! summary "Recap" 
    
    **repo:** 

    **commit:** Git equivalent of "save"

### Attribution

The material in this section is based on following courses:
- Software Carpentry Lesson [Version Control with Git](http://swcarpentry.github.io/git-novice/)
- Coderefinery [Introduction to Git](https://coderefinery.github.io/git-intro/)
