# Repository

A Git Repository ("Repo") is a workspace that tracks and manages files within a folder.

# Commiting

>Commiting is the **most** important Git 
feature.

A Commit is equivalent to taking a snapshot of the repository at a given time. When commiting we can save the state of multiple files and folders.

## Basic workflow

1. Work on Stuff.
2. Add changes.
3. Commit

### 1. Work on Stuff

The command **git status** gives information on the status of the current repository.

Start a new repository on the top-level folder for your project with the command **git init**.

>Do not start repositories inside a repository!

Before using **git init** run **git status** to make sure you are not inside a repository.

You can now add, delete, rename, edit files and directories in your project.

### 2. Add Changes.

Once you are ready you can use **git add** to stage the canges to be commited.

you can use **git add .** to add all changed files to staging or **git add file1 file2 .. fileN** to add specific files to staging.

>Use **git status** to constantly verify what changes are staged amd not staged!

### 3. Commit

Use **git commit** to actually commit the changes from the staging area.

```sh
# Commit all staged changes
git commit

# add description message
git commit -m "Message"
```

In case you forgot a file or need to edit the commit message. You can **ammend** the last commit

```sh
# amend commit
git commit -m "Messge"
git add missed_file
git commit --amend 
```
