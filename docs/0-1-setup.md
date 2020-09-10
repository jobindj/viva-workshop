# **Pre-workshop installation**

## **1. Install Git**

_If you already have a working installation of Git on your system, you can skip this step._ 

To install Git, please follow these instructions on the OpenVT platform

-  install Git on [Linux](https://virtual.openvt.eu/platform_manual_and_guidelines/manual_and_guidelines/wikis/installing-git:-Linux) or 
-  install Git on [Windows](https://virtual.openvt.eu/platform_manual_and_guidelines/manual_and_guidelines/wikis/Installing-git:-Windows).

### **A | Configuring Git user name and email**

You will need to configure your name and email.

For this, open a Terminal (as Linux user) or open the Git Bash app (on Windows). Type the following, where you replace <your_email> and <your_username> with the data you are signed up with on OpenVT:
```
git config --global user.name <your_username>
git config --global user.email <your_email>
```

### **B | Create an SSH to connect with OpenVT**

You will need to setup SSH key for your OpenVT account. Follow [these instructions on OpenVT Manual](https://virtual.openvt.eu/platform_manual_and_guidelines/manual_and_guidelines/wikis/Getting-started-with-Git#creating-an-ssh-key) to setup your SSH key

To test whether your SSH key was added correctly, run the following command in your terminal

```
ssh -T git@virtual.openvt.eu
```
You should receive a Welcome to GitLab, @username! message.

### C | (Optional) Git GUI options

The Git workflow will be illustrated using the command line in the workshop. 

If you are more comfortable using GUI instead of command line, there are many [Git GUI clients](https://git-scm.com/downloads/guis) available. 

<!-- _Git workflow using [Git Extensions](http://gitextensions.github.io/) GUI client will be provided in the handouts. You are welcome to explore this at your pace after the workshop._ -->


## **2. Install Jupyter Notebook**

If you have already a working installation of Jupyter Notebook together with [Dynasaur](https://gitlab.com/VSI-TUGraz/Dynasaur) on your system, you may skip this step. Otherwise you can find further information about the installation on the following [page](0-jupyter-notebook-setup.md).