# Working with Remote Repo

!!! summary "Overview" 

    **Questions**
  
    **Objectives** 
  
   

## Create an Issue

## Pull the latest version of the repo

```
git pull
```

```
git pull --rebase
```

### Fetch

Use the online interface

### Merge/Rebase

## Switch to your branch and edit the README

We are going to be using the branch you created during the pre-workshop setup

```
git checkout FirstName-LastName
```

Edit the README.md to add your name to the list of workshop participants. Add the following line to link you name on the README to the file with your details.
[FirstName LastName](FirstName-LastName.md)

When you `git status`, it will show that README has been modified. Add the README also to the staging area using `git add`

```
git add README.md
```

Commit the changes to the README using `git commit`

## Push

Now you are ready to push the changes you made in your branch to the remote repo

```
git push orgin FirstName-LastName
```

## Submit a Merge Request

Using the issue number

## More Resources

- [Graphical Interactive cheatsheet](https://ndpsoftware.com/git-cheatsheet.html)