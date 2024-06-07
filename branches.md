# Branches

Branches are alternative timelines of a project.

Branches enable us to create separate contexts where we can try new things, or even work on multiple ideas in paralell.

>Changes to one branch do not impact changes to another branch (unless changes are merged!).

In Git we are always working in one branch. The default branch is called **Master** or **Main**.

## HEAD

**HEAD** is a pointer that refers to the current "location" in your repository. It points to a particular branch reference.

## Viewing Branches

Use **git branch** to view your existing branches. The default branch in the repo is Master or Main.

Look for the *. It indicates the branch you are currently on.

## Creating a new Branch

To make a new branch based on the current HEAD.

```sh
# Create a new branch, does not switch to it (HEAD stays the same)
git branch <branch-name>
```

### Switch Branches

When switching branches the HEAD will now point to the new branch.
Any new commits will only exist on the branch we switched to.

```sh
git switch <branch-name>
```

An alternative option is to use **checkout**

```sh
git checkout <branch-name>
```

### Create and Switch to new Branch

By using **-c** flag with the **git switch** command a new branch will be created and the HEAD will be moved to the new Branch

```sh
git switch -c <branch-name>
```

### Viewing more info

To view additional information on a Branch use **-v** flag

```sh
git branch -v
```

### Rename a Branch

- Rename current branch

    ```sh
    git branch -m <newName>
    ```

- Rename branch while pointed to another branch

    ```sh
    git branch -m <oldName> <newName>
    ```

- Push local branch and reset the upstream

    ```sh
    git push origin -u <newName>
    ```

- Delete remote branch

    ```sh
    git push origin --delete <oldName>
    ```

- Delete the old-name remote branch and push the new name local branch

    ```sh
    git push origin :<oldName> <newName>
    ```

- Unset the upstream

    Make sure you run command **git status** and check that the newly created branch is pointing to its own ref and not the older one. If you find the reference to the older branch, you need to unset the upstream using:

    ```sh
    git branch --unset-upstream
    ```

- Reset the upstream branch for the newName local branch

    ```sh
    git push origin -u <newName>
    ```
