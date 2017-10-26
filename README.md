# GitHub Tutorial

_By Jennifer Liu_

---
## Git vs. GitHub  

Git: keeps "snapshots" of your codes  
**Does not require Github**  
Github: stores code in the cloud, which is known as [Github](https://github.com/)  
**Requires Git**  

---
## Initial Setup
**_Creating a Github account:_**
1. Go to [Github](https://github.com)
2. Click **Sign Up** on the top-right corner and after you click **Sign Up**, you will see the following:
    ![first-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/first-step-setup.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)  
    1. Finish all 3 steps

3. You may choose your plan and if you want to receive updates from Github through emails by selecting the boxes
![second-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/second-step-setup.png?_c9_id=livepreview2&_c9_host=https://ide.c9.io)
4. After you click **Continue**, you will see the following:
    ![third-step-setup](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/third-step-setup.png?_c9_id=livepreview7&_c9_host=https://ide.c9.io)
    1. You may choose to **skip this step** or fill out the survey and **submit**

**_SSH Key:_**
1. Click on **your profile** and go to **settings** then click on **SSH and GPG Keys**
    1. ![ssh-key-1](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/ssh-key-1.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)
2. Click on **New SSH Key** and name it **cloud9** because the SSH Key should connect with cloud9 for coding and allows you to `git push` (sending commits from the local repo [cloud9] to remote repo [Github]
    1. On your cloud9 click on **settings** and you will find **SSH Keys**. You will copy the SSH Key code from cloud9 to Github and _add the SSH Key_
    2. ![ssh-key-2](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/ssh-key-2.png)
3. Now when you reopen cloud9, it will tell you that you are connected to Github

4. When you create a new repository and clone to your cloud9, you should make sure your SSH Key is selected and copy and paste
    1. ![ssh-key-3](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/ssh-key-3.png)
    2. ![ssh-key-4](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/ssh-key-4.png)


---
## Repository Setup  
**_Creating a repository on Github:_**
1. Click on the **add** icon
    1. ![repo-setup-1](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/repo-setup-1.png)
2. Give your repository a name and add description if you want and click on **Create repository**
    1. ![repo-setup-2](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/repo-setup-2.png?_c9_id=livepreview3&_c9_host=https://ide.c9.io)  
3. Now, go to your c9 workspace
4. Make a new repository by `mkdir <reponame>` **The repo name should match the name you created in Github**
5. Type `cd <reponame>` and this means moving into this repository 
6. After you are in the repository, type `git init`
    1.  When you are in your workspace, you should **NEVER EVER** `git init` in your **_workspace_**
    2. `git init` (initialize git for version control, taking snapshots of your codes)
    3. ![git-init](https://preview.c9users.io/jenniferl4209/github-learning/github-tutorial/git-init.png?_c9_id=livepreview4&_c9_host=https://ide.c9.io)
    4. when you see **(master)**, this means that your directory is initialized
7. Type `touch README.md` to create a new file 
8. Type `git add README.md` to add the file to the stage 
9. Type `git commit -m "message"` for the first commit
10. Go back to Github and copy and paste `git remote add origin <url>` 
11. Lastly, type `git push -u origin master` **This is pushing commits from cloud9 to Github**  
_Woo hoo! You just created a new repository on your Github!_

---
## Workflow & Commands
**_Git Status:_**
1. a command to see which files have been edited since their last commit and which files are staged to commit 
2. `git status` is how you will see the files that have been edited or to be commited
    1. **Untracked:** the file is in the directory, but it is _not_ in the staging area
    2. **Modified:** the file is _added_ to the staging area and there are _changes_ to the file
    3. **Tracked/Staged:** the file is in the staging area _waiting to be commited_

**_Git Add:_**
1. a command that adds files to the stage area waiting to be commited
    1. `git add <filename>` is how to add files
    2. `git add .` alls all existing files
    3. `git add --all` adds all files including deleted files

**_Git Commit:_**
1. a command that takes snapshot of codes and use a short/specific message to explain the code
2. `git commit -m "message"`the message should be in quotations

**_Git Push:_**
1. a command that sends commits from the local repo (cloud9) to the remote repo (Github)
2. In order to `git push`:
    1. `git remote add origin URL`:
        1. setting up a **connection** with the crrent repo and the external repo (Github) and origin is the nickname for the remotes
        2. URL is the **link** of the location of the remote repo
    2. `git push -u origin master`:
        1. **-u** allows git to remember which remote to push when you type `git push` in the future
        2. **origin** is the remote repo we are pushing to
        3. **master** is the branch of the project (you always see **master** when you initialize git)
    3. After these commands, you can `git push` to send commits to Github now  

_Woo hoo! You just learned how to push commits to Github!_

---
## Rolling Back Changes
**_Undo Edits:_**
1. The purpose is that if you are working a project with someone, and you edit the file that may cause conflicting problems later, you can **undo the edits**
2. After you make changes to your file, type `git status`
3. You will see: `git checkout <filename>`
4. Type `git checkout <filename>` to undo the edit you made

**_Undo Adds:_**
1. The purpose is that you may have edited two files and added both to the stage. However, you only wanted to add one file to the stage, and now you need to remove the file from the stage 
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
4. Copy the **SHA**
5. Press Q to quit and type `git revert <SHA>`
6. After `git revert <SHA>`, you will see the following:
7. Press Control X to exit and choose **Y** if you want to save the change or **N** if you don't want to undo the push  

_Woo hoo! You just learned how to undo your pushed commit!_

---
## Error Handling
1. If you accidentally `git init` in your workspace, you may do `rm -rf. git` to uninitialize Git











































































