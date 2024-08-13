# PLPBasicGitAssignment
attempting  a hands on training

Here's a draft for your `README.md` file that documents the steps and commands used, including the issues and solutions encountered during the assignment:


# Git and GitHub Basic Assignment

## Overview

This repository contains the basic steps and commands used to complete a Git and GitHub assignment. The goal was to create a repository, add a file, commit changes, and push them to GitHub.

## Steps and Commands

### 1. Initialize Git Repository

First, we initialized a new Git repository in the local directory:

git init


### 2. Create and Add a File

We created a new text file named `hello.txt` and added a simple text message:


echo "Hello, Git!" > hello.txt


Then, we staged the file for commit:


git add hello.txt


### 3. Commit Changes

We committed the changes with a descriptive message:


git commit -m "Add hello.txt with a greeting"


### 4. Configure Remote Repository

We added a remote repository URL:


git remote add origin https://github.com/josephkplp/PLPBasicGitAssignment.git


### 5. Push Changes

Initially, there were issues pushing changes due to mismatched branch names and unrelated histories. Here's how we resolved them:

#### Renaming Branch

The default branch was `master`, but the remote repository used `main`. We renamed the local branch:


git branch -m master main

#### Handling Unrelated Histories

When pushing, we encountered an error due to unrelated histories. We resolved it by pulling with the `--allow-unrelated-histories` flag:


git pull origin main --allow-unrelated-histories


#### Resolving Merge Conflicts

We resolved any merge conflicts (if they arose) and committed the resolved changes:


git add hello.txt
git commit -m "Resolve merge conflicts"


#### Final Push

After resolving conflicts and ensuring everything was in order, we pushed the changes:


git push -u origin main


### Issues Encountered

- Unrelated Histories: We had to use the `--allow-unrelated-histories` flag to merge the histories of the local and remote repositories.
- Non-Fast-Forward Error: This was due to the remote branch having commits that our local branch did not. We had to pull changes first and resolve any conflicts.

### Summary

- **Commands Used**: Documented above.
- **Issues Resolved**: Merging unrelated histories and resolving non-fast-forward errors.

## Repository URL

The repository can be accessed at: [GitHub Repository](https://github.com/josephkplp/PLPBasicGitAssignment)

## Additional Notes

- For further troubleshooting, refer to the [GitHub documentation](https://docs.github.com/en).
- Seek assistance from peers or instructors if additional issues arise.


By following these documented steps, the assignment was successfully completed, demonstrating basic Git and GitHub workflows.

