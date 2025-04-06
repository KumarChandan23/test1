# Git
- Git is version control system that helps you trach changes in your code and collaborate with others

# 🏗️ Git terms & Concepts
- Repository(Repo): A folder where git trachs our changes in code.
- Commit: A snapshort of our project at specific time.
- Branch: A separate line of development ( like trying somethings new without affecting main project).
- Merge: Combining chages from one branch ot other.
- Clone: Copy of remote repository to our local computer.
- Push: Send your local changes to remote repository.
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

# Git Command
2. git branch new-feature : create new branch.
3. git checkout new-feature : switch to new brach.
4. git checkout -b new-feature : create and switch to new branch.
5. git merge branch-name : merge branch into current branch. 
6. git branch -d branch-name : delete branch if merged.
7. git branch -D branch-name : delete branch even if not merged.

# List branch
1. git branch / git branch --list : shows list of all branches.
2. git branch -r : list all remote branches.
3. git branch -a : list all local and remote branches
4. git branch -m new-name : Rename current branch
5. git branch -m old-name new-name : Rename any branch

# Push Branch 
1. git push -u origin <branch-name>

# Git Rebase
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



