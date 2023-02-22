# Revisions and the Cloud

## What is version control?

Version Control is a system that records changes to a file or set of files over time so that you can recall specific versions later. It helps you keep track of changes made to your code or documents, collaborate with other team members, and revert to previous versions if necessary. It also enables you to branch your codebase and work on multiple features simultaneously.

***

## What is cloning in Git?
Cloning in Git refers to the process of creating a copy of a repository on your local machine. When you clone a repository, you create a complete copy of the project, including all its files, commits, and branches. Cloning allows you to work on the project on your local machine, make changes, and push those changes back to the remote repository.

***

## What is the command to track and stage files?

>`git add`

The command to track and stage files in Git is "git add". This command adds changes to the staging area, which is a temporary storage location for changes you want to commit to your repository. For example, if you want to add a file named "example.txt" to the staging area, you would run the command `git add example.md`

***

## What is the command to take a snapshot of your changed files? 

> `git commit`

The command to take a snapshot of your changed files in Git is "git commit". This command creates a new commit, which is a snapshot of your changes at a specific point in time. When you run this command as `git commit -m "EXAMPLE CONTEXT"` you can enter a commit message that describes _why_ you made the changes you made.

***

## What is the command to send your changed files to GitHub?

> `git push` 

The command to send your changed files to GitHub is a series of Git commands that involve pushing your changes to the remote repository. You need to push your changes using the command `git push origin main` to push your changes to a repo named "origin" on GitHub. 