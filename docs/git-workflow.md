# Basic Git Workflow


## Visualizing the Workflow

http://git-school.github.io/visualizing-git/

Try the following steps one-at-a-time in the visualization window
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