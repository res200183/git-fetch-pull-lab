# Git Fetch vs Git Pull Practice

This repository demonstrates the practical difference between git fetch and git pull. The goal of this practice was to understand how a local Git repository interacts with a remote repository on GitHub and how developers synchronize changes between them.

During this exercise the following tasks were performed: cloning a repository from GitHub, configuring the remote repository, creating commits locally on an AWS EC2 instance, pushing commits to GitHub, using git fetch to download remote changes, inspecting remote commits using git log origin/main, comparing local and remote branches, merging remote changes using git merge origin/main, and updating the repository using git pull.

The key concept demonstrated in this repository is the difference between git fetch and git pull. The command git fetch downloads new commits from the remote repository but does not modify the local working branch. Instead, it updates the remote-tracking branch such as origin/main. This allows developers to safely inspect incoming changes before applying them.

In contrast, git pull downloads the changes and immediately applies them to the current branch. In most configurations git pull is effectively a combination of two commands: git fetch followed by git merge. Because of this behavior, git pull modifies the working branch automatically.

Many developers prefer using git fetch first because it provides more control over the update process. After fetching changes, developers can review commits, inspect differences, and decide whether to merge or rebase the changes. A common workflow therefore looks like this: first run git fetch, then inspect commits using git log origin/main, and finally apply the changes with git merge origin/main.

This practice was performed using Git, GitHub, AWS EC2 running Amazon Linux, and SSH authentication for secure interaction with the remote repository.
