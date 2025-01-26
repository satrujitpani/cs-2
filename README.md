Case Study: Resolving Merge Conflicts

📌 Project Overview

This case study focuses on resolving merge conflicts in Git. You are working for Zendrix Software & Co., where the company follows a monolithic architecture, and all the code resides in a single file, main.c. Your task is to update the master branch with changes from feature branches while ensuring all conflicts are resolved properly.

🎯 Problem Statement

The master branch received a security patch update.

Two feature branches (feature1 and feature2) were created before the security patch, making them behind the master branch by 1 commit.

Your objective is to:

Update feature1 and feature2 branches with the latest security patch.

Merge feature1 and feature2 changes into master, handling any merge conflicts.

Push all updated branches to GitHub.

🛠 Steps to Solve the Case Study

1️⃣ Fork & Clone the Repository

# Fork the repository to your GitHub account
# Clone the repository to your local system

git clone https://github.com/devops-intellipaat/merge-conflict.git
cd merge-conflict

2️⃣ Update Feature Branches with Security Patch

# Checkout feature1 branch
git checkout feature1

# Merge master into feature1
git merge master

# Resolve conflicts (if any), then commit
# After resolving conflicts, stage and commit

git add main.c
git commit -m "Merged security patch from master into feature1"

git checkout feature2

git merge master

git add main.c
git commit -m "Merged security patch from master into feature2"

3️⃣ Merge Feature Branches into Master

# Switch to master branch
git checkout master

# Merge feature1 into master
git merge feature1
# If there are conflicts, resolve them, then:
git add main.c
git commit -m "Merged feature1 into master"

# Merge feature2 into master
git merge feature2
# Resolve conflicts if needed, then:
git add main.c
git commit -m "Merged feature2 into master"

4️⃣ Push Changes to GitHub

git push origin master
git push origin feature1
git push origin feature2

📂 Repository Structure

merge-conflict/

│── main.c
│── README.md (this file)

🚀 Final Outcome

The master branch now includes all the latest updates from feature1 and feature2.

Any merge conflicts were resolved manually.

The updated repository has been pushed to GitHub.

📝 Conclusion

This case study demonstrates how to efficiently resolve merge conflicts, apply updates, and keep feature branches in sync with the master branch. Handling conflicts effectively is a crucial skill in collaborative Git workflows.

