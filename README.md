# Git Setup and Repository Workflow on AWS Linux (YUM Based System)

This document explains how to install Git, configure it, and manage a GitHub repository step by step on a YUM-based Linux instance.

---

## 1. Update System Packages
```bash
sudo yum update -y
```
Updates all installed packages to the latest version.  
This ensures the system is secure and up to date before installing Git.

---

## 2. Install Git
```bash
sudo yum install git -y
```
Installs Git on the system.  
The `-y` flag auto-confirms the installation prompts.

---

## 3. Configure Git (Global Settings)
```bash
git config --global user.name "Saikiran Asamwar"
git config --global user.email "saikiranasamwar@gmail.com"
git config --list
```
Sets your Git username and email globally for all repositories.  
`git config --list` verifies that the details are correctly configured.

---

## 4. Clone Repository
```bash
git clone https://github.com/SaikiranAsamwar/Demorepo.git
ls
```
Downloads a copy of the repository from GitHub to your instance.  
`ls` confirms that the repository folder is created.

---

## 5. Navigate to Repository
```bash
cd Demorepo/
```
Moves into the cloned repository folder.  
All further Git commands will be run inside this directory.

---

## 6. Branch Management
```bash
git branch
git branch dev
git checkout dev
git branch
```
`git branch` lists existing branches.  
A new branch `dev` is created and switched to for development.

---

## 7. Create and Edit a File
```bash
touch index.py
sudo nano index.py
cat index.py
python3 index.py
```
Creates a new Python file named `index.py`.  
It is edited with `nano`, displayed using `cat`, and executed with Python.

---

## 8. Git Workflow
```bash
git status
git add .
git status
git commit -m "new file added"
git push origin dev
git pull
```
`git status` shows changes in the repo.  
Files are staged with `git add`, committed with a message, pushed to GitHub, and `git pull` fetches the latest updates.

---

## 9. View Command History
```bash
history
```
Displays all previously executed commands in the current shell.  
Helps in tracking or documenting the steps taken.

---

## 10. Collaboration Workflow (With Teammate Repo)

This section explains how to collaborate with a teammate’s repository.

---

### a) Clone Teammate’s Repository
```bash
git clone https://github.com/Khushal41/Demorepo.git
ls
cd Demorepo/
ls
```
Clones your teammate’s repository to your system.  
Verifies the folder structure using `ls` and navigates inside it.

---

### b) Branch Management
```bash
git branch
git branch dev
git branch
git checkout dev
ls
```
Lists available branches and creates a new `dev` branch.  
Switches to `dev` branch where development changes will be made.

---

### c) Create and Edit a File
```bash
touch index.py
sudo nano index.py
cat index.py
python3 index.py
```
Creates `index.py`, edits it with `nano`, prints the content, and runs it with Python.  
This verifies that the file works as expected before committing.

---

### d) Git Workflow (Collaboration)
```bash
git status
git add index.py
git status
git commit -m "New file added"
git push origin dev
git pull
```
Checks the repo status, stages the new file, and commits it with a message.  
Pushes changes to the remote `dev` branch and pulls any updates from GitHub.

---

### e) View Command History
```bash
history
```
Displays the command history for collaboration steps.  
Useful for tracking exact actions taken during teamwork.

---

## Author
**Saikiran Asamwar**  
GitHub: [SaikiranAsamwar](https://github.com/SaikiranAsamwar)
