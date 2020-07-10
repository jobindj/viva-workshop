# Basic Git Workflow on Local Repo


## Visualizing the Workflow

In this section and the next, you will learn how to make commits in your local repo and how to share it with a remote repo. Before we go into details, it is helpful to get a bigger picture of the workflow by visualizing a git workflow for collaborative development. Try the following steps on http://git-school.github.io/visualizing-git/

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