# Git & Cloud Server Setup Guide

## Git Basic Commands

git add .  
# Save changes to staging

git commit -m "message"  
# Prepare commit before pushing

git push origin [branch-name]  
# Push code to GitHub repository

git pull  
# Fetch and merge latest changes into local

---

## Common git push Flags

-u, --set-upstream  
Link your local branch to a remote branch

-f, --force 
Overwrite remote history (dangerous)

--tags  
Push all local tags

--delete  
Delete a branch on remote  
Example: git push origin --delete feature-branch

---

## Common git pull Flags

--rebase  
Reapply commits on top of remote changes (clean history)

--ff-only  
Only allow fast-forward merge

--no-commit  
Merge but stop before committing

--squash  
Combine commits into one

---

## Deploy Server on Google Cloud

### 1. Install LAMP Stack
- Linux
- Apache
- MySQL
- PHP

---

### 2. Setup GitHub with SSH

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"  
# Generate SSH key

cat ~/.ssh/id_rsa.pub  
# Copy key and add to GitHub

---

### 3. (Optional) Create New User

sudo adduser username

---

### 4. Clone Project from GitHub

git clone git@github.com:username/repository.git

---

### 5. Redirect Web Root

Default Apache directory:
/var/www/html

Link your project:

sudo ln -s /path-to-your-project /var/www/html

---

## Important Linux Commands

mkdir folder_name  
# Create directory

rmdir folder_name  
# Delete directory

nano filename  
# Create or edit file

---

## ln Command

ln [OPTIONS] <TARGET> [LINK_NAME]

Options:
-s   Create symbolic link  
-f   Force overwrite  
-i   Ask before overwrite  

---

## Notes

LAMP = Linux + Apache + MySQL + PHP  
CRUD = Create, Read, Update, Delete  

---
