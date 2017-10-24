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
1. Go to [Github](https://github.com/) **_"I changed the link cause your original link doesnt work"_**
2. Click **Sign Up** on the top-right corner and after you click **Sign Up**, you will see the following:
    ![first-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/first-step-setup.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)  
    1. Finish all 3 steps

3. You may choose your plan and if you want to receive updates from Github through emails by clicking on the boxes
![second-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/second-step-setup.png?_c9_id=livepreview2&_c9_host=https://ide.c9.io)
4. After you click **Continue**, you will see the following:
    ![third-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/third-step-setup.png?_c9_id=livepreview7&_c9_host=https://ide.c9.io)
    1. You may choose to **skip this step** or fill out the survey and **submit**

**_SSH Key:_**
1. Click on _your profile_ and go to _settings_ then click on **SSH and GPG Keys**
    1. ![ssh-key-1](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/ssh-key-1.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)
2. Click on _New SSH Key_ and name it _cloud9_ because the SSH Key should connect with cloud9 for coding and allows you to `git push` (sending commits from the local repo [cloud9] to remote repo [Github]
    1. On your cloud9 click on **settings** and you will find **SSH Keys**. You will copy the SSH Key code to Github and _add_. 
3. Now when you reopen cloud9, it will tell you that you are connected to Github

**When you create a new repository and clone to your cloud9, you should make sure your SSH Key is selected and copy and paste the ...** _I am not sure what you mean by the "..."_  


---
## Repository Setup  
"I am not sure if you've done the repository setup correctly cause I dont think we suppose to talk about `git clone` in this part. Look at slides 3 through 6 in 10/3 slides on how we should do the setup"  
**_Creating a repository on Github:_**
1. Click on the **add** icon
    1. ![repo-setup-1](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/repo-setup-1.png?_c9_id=livepreview2&_c9_host=https://ide.c9.io)
2. Give your repository a name and add description if you want and click on **Create repository**
    1. ![repo-setup-2](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/repo-setup-2.png?_c9_id=livepreview3&_c9_host=https://ide.c9.io)  

###### _Woo hoo! You just created a new repository on your Github!_

3. Now you should **clone** your repository to c9
    1. ![clone](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/clone.png)


##### **_Initialize Your Repository:_**
1. Sign in to your c9 account and open up you workspace
2. When you are in your workspace, you should **NEVER EVER** `git init` in your **_workspace_** "Optional: you can tell how to uninitialize git if you accidentally initialized it in your workspace"
3. You should `cd` into the directory, or folder (Github: repository) you are working in right away
    1. Git init (initialize git for version control, taking snapshots of your codes)
    2. ![git-init](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/git-init.png?_c9_id=livepreview4&_c9_host=https://ide.c9.io)
    3. when you see **(master)**, this means that your directory is initialized

**_Git Add:_**
1. `git add <filename>` means adding a file to the staging area to be commited

**_Git Commit_**
1. `git commit -m "message"` means taking a "snapshot" of the file(s) you've added to the stage
    1. should be in the present tense
---
## Workflow & Commands
**_Git Status:_**
1. a command to see which files have been edited since their last commit and which files are staged to commit 
2. `git status` is how you will see the files that have been edited or to be commited

**_Git Add:_**
1. a command that adds files to the stage area waiting to be commited
2. `git add <filename>` is how to add files

**_Git Commit:_**
1. a command that takes snapshot of codes and use a short/specific message to explain the code
2. `git commit -m "message"`the message should be in quotations

**_Git Push:_**
1. a command that sends commits from the local repo (cloud9) to the remote repo (Github) 
2. In order to `git push`:
    1. `git remote add origin URL`:
        1. setting up a connection with the crrent repo and the external repo (Github) and origin is the nickname for the remotes
        2. URL is the link of the location of the remote repo
        3. _By doing this, you can git push now_ [see below]
    2. `git push -u origin master`:
        1. -u allows git to remember which remote to push when you type `git push` in the future
        2. origin is the remote repo we are pushing to
        3. master is the branch of the project (you always see **master** when you initialize git)
    3. After these commands, you can `git push` to send commits to Github now  

_Woo hoo! You just learned how to push commits to Github!_

---
## Rolling Back Changes
**_Undo Edits:_**
1. The purpose is that if you are working a project with someone, and you edit the file that may cause conflicting problems later, you can **undo the edits**
2. After you make changes to your file, type `git status`
3. You will see:
4. Type `git checkout <filename>` to undo the edit you made

**_Undo Adds:_**
1. The purpose is that you may have edited two files and added both to the stage. However, you wanted to add one file to the stage, and now you need to remove the file from the stage 
2. Type `git add <filename>` and do `git status`
3. In the git status, you will see that the file is _green_
    1. Above the file, it said `git reset HEAD <filename>`
    2. Type that and do `git status` again
    3. You will see that the file is _red_  

_You just remove the file from the stage!_ 

**_Undo Commits:_**
1. Sometimes, you just don't want to take a snapshot of your codes at the moment. Luckily, you can **undo a commit**!
2. `git log` shows all your commits in a list and the commit and the **top** is the most recent one
3. Press Q to quit `git log`
3. After you see your latest commit, type `git reset --soft HEAD~1`
4. Type `git log` again  

_OMG! Did you see that your latest commit is **GONE**?_  
`git reset --soft HEAD~1` is your **git saver :)**

**_Undo Push:_**
1. When you push your commit to Github, but this may ruin your collaborator's code if what you commit is crushing theirs. No worries! You can **undo your push!**
2. After you type `git push`, type `git log`
3. Your latest commit have a series of numbers, which is the **SHA**
4. Press Q to quit and type `git revert <SHA>`
5. After `git revert <SHA>`, you will see the following:
6. Press Control X to exit and choose **Y** if you want to save the change or **N** if you don't want to undo the push  

_Woo hoo! You just learned how to undo your pushed commit!_








































































