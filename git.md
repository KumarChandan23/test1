# Git
- Git is version control system that helps you trach changes in your code and collaborate with others

# 🏗️ Git terms & Concepts
- Repository(Repo): A folder where git trachs our changes in code.
- Commit: A snapshort of our project at specific time.
- Branch: A separate line of development ( like trying somethings new without affecting main project).
- Merge: Combining chages from one branch ot other.
- Clone: Copy of remote repository to our local computer.
- Push: Send your local changes to remote repository.
- HEAD: A pointer to current branch reference.
- staging Area (Index): A place where we prepare change befor commiting.
- Working Directoty: Actual project folder where we edit changes.
- Origin: The defoult name for remote repogitory.
- Pull: Get latest changes from Github to out local computer.
- Remote: The version of our repository on Github (online).
- Local: The version of our own computer
- Fork : Copy someone else's repo to your account.
- Pull Request(PR) : Propose changes to someone’s repo.
- .gitignore : A file where we list what Git should igonre
- Conflict : when two people edit the same part of file 

# 💻 What is GitHub?
- Github is website where we can store our Git repository online. 
- It is same like cloud space.

# 🧠 Why use GitHub?
- Backup our code online.
- Share our project with others
- Work on same project with our team form different location.
- Showcase our project to the world

# 🔄 Git & GitHub Workflow (Simple Steps):
1. Install Git on your computer Go to https://git-scm.com/ and download it.

# Basic Git Commands (used in terminal):
1. git init : Create a new git repo
2. git status : Check current status
3. git add . : Add all files to staging (ready to commit)
4. git commit -m "Initial commit" : Save changes with a message
5. git remote add origin https://github.com/your-username/your-repo.git : Connect to GitHub repo
6. git push -u origin main/master : Push your code to GitHub

# Undo git initialization or Delete git folder
1. rd /s /q .git => used in cmd
2. Remote-Item -Resource -Force .git => used in powershell

# 🌳 Branching 
- A branch it pointer to a snapshort of our changes.
- The default git branch is master or main.
- we use branches to develope new feature, fix bugs or without affecting main branch

# Branch Commands
2. git branch new-feature : create new branch.
3. git checkout new-feature : switch to new brach.
4. git checkout -b new-feature : create and switch to new branch.
5. git merge branch-name : merge branch into current branch. 

# Push Branch 
1. git push -u origin <branch-name>

# List branch
1. git branch / git branch --list : shows list of all branches.
2. git branch -r : list all remote branches.
3. git branch -a : list all local and remote branches
4. git branch -m new-name : Rename current branch
5. git branch -m old-name new-name : Rename any branch

# 🌐 Delete branch
1. git branch -d branch-name : delete local branch if merged.
2. git branch -D branch-name : delete local branch forcefully even if not merged.
3. git push origin --delete branch-name : delete branch remote

# 🧠 Stale tracking branch?
- A brach which is deleted form the remote but still it is available in local is known as stale branch.
- When we work with remote branch, git keep local reference to remote branch
- if some deletes remote branch form Github, git does not deletes it from local list.
- To delete those branch locally we use this 
- Command: 
        - git remote prune origin --dry-run : it shows all stale branch before deletion
        - git remote prune origin : delete all local branch which not on remote 

# 🔄 Restore a deleted branch
 For local branch 
- git reflog : This shows history of everything you did, including deleted branch.
- git checkout -b feature/login <commit hash -> abc1234>

# 📊 Visualization Tip
- it shows all history
- git log --oneline --graph --all --decorate


# ⚙️ Git Rebase
- Keeps history clean and reable
- It makes feature merges easier
1. git checkout feature : branch switch
2. git rebase main : This reapplies commit from current branch on top of the main branch.
3. git push --force : forcefully push
- feature branch
    A---B---C   ← main
             \
              D---E   ← feature
- A, B, C: Commits on main
- D, E: Commits on your feature branch (based on an old main)
💬 Now you run rebase and get this  
- A---B---C---D'---E' 

#  Squash commits during rebase
- Squashing means combining multiple commits into a single one.
- we do this during intratice rebase, typically to clean up small or messy commit before mearing a feature 
- git rebase -i HEAD~3
- Example : 
    - Before : A---B---C---D---E  (feature)
    - git rebase -i HEAD~3
    - After : A---B---C'  (feature)

# Delete remote branch
- git push origin --delete <branch-name>



