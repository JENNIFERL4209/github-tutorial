# GitHub Tutorial

_By Jennifer Liu_

---
## Git vs. GitHub
Git: keeps "snapshots" of your codes  
**Does not require Github**  
Github: stores code in the cloud, which is known as [Github](www.github.com)  
**Requires Git**

---
## Initial Setup
**_Creating a Github account:_**
1. Go to [Github](www.github.com)
2. Click **Sign Up** on the top-right corner and after you click **Sign Up**, you will see the following:
    ![first-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/first-step-setup.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)  
    1. Finish all 3 steps

3. You may choose your plan and if you want to receive updates from Github through emails by clicking on the boxes
![second-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/second-step-setup.png?_c9_id=livepreview2&_c9_host=https://ide.c9.io)
4. After you click **Continue**, you will see the following:
    ![third-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/third-step-setup.png?_c9_id=livepreview7&_c9_host=https://ide.c9.io)
    1. You may choose to **skip this step** or fill out the survey and **submit**

**_SSH Key:_**
1. Click on _your profie_ and go to _settings_ then click on **SSH and GPG Keys**
    1. ![ssh-key-1](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/ssh-key-1.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)
2. Click on _New SSH Key_ and name it _cloud9_ because the SSH Key should connect with cloud9 for coding and allows you to `git push` (sending commits from the local repo [cloud9] to remote repo [Github]
    1. Click on **settings** and you will find **SSH Keys**. You will copy the SSH Key code to Github and _add_. 
3. Now when you reopen cloud9, it will tell you that you are connected to Github

**When you create a new repository and clone to your cloud9, you should make sure your SSH Key is selected and copy and paste the ...**

---
## Repository Setup
**_Creating a repository on Github:_**
1. Click on the **add** icon
    1. ![repo-setup-1](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/repo-setup-1.png?_c9_id=livepreview2&_c9_host=https://ide.c9.io)
2. Give your repository a name and add description if you want and click on **Create repository**
    1. ![repo-setup-2](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/repo-setup-2.png?_c9_id=livepreview3&_c9_host=https://ide.c9.io)  

###### _Woo hoo! You just created a new repository on your Github!_

3. Now you should **clone** your repository to c9
    1. ![clone](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/clone.png)


##### **_Initialize Your Repository:_**
1. Sign into your c9 account and open up you workspace
2. When you are in your workspace, you should **NEVER EVER** `git init` in your **_workspace_**
3. You should `cd` into the directory, or folder (Github: repository) you are working in right away
    1. Git init (initialize git for version control, taking snapshots of your codes)
    2. ![git-init](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/git-init.png?_c9_id=livepreview4&_c9_host=https://ide.c9.io)
    3. when you see **(master)**, this means that your directory is initialized

**_Git Add:_**
1. `git add <filename>` means adding a file to the staging area to be commited

**_Git Commit_**
1. `git commit -m "message"` means taking a "snapshot" of the file you currently edited
    1. should be in the present tense








---
## Workflow & Commands



---
## Rolling Back Changes