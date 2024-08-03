# Git Commands

## Overview
- [Git Commands](#git-commands)
  - [Overview](#overview)
  - [Initializing a Repository](#initializing-a-repository)
  - [Cloning a Repository](#cloning-a-repository)
  - [Checking Repository Status](#checking-repository-status)
  - [Adding Files to Staging Area](#adding-files-to-staging-area)
  - [Committing Changes](#committing-changes)
  - [Viewing Commit History](#viewing-commit-history)
  - [Creating a Branch](#creating-a-branch)
  - [Switching Branches](#switching-branches)
  - [Merging Branches](#merging-branches)
  - [Pushing Changes to Remote](#pushing-changes-to-remote)
  - [Pulling Changes from Remote](#pulling-changes-from-remote)
  - [Fetching Changes from Remote](#fetching-changes-from-remote)
  - [Reverting Changes](#reverting-changes)
  - [Stashing Changes](#stashing-changes)
  - [Applying Stashed Changes](#applying-stashed-changes)
  - [Deleting a Branch](#deleting-a-branch)
  - [Viewing Remote Repositories](#viewing-remote-repositories)
  - [Adding a Remote Repository](#adding-a-remote-repository)
  - [Removing a Remote Repository](#removing-a-remote-repository)

## Initializing a Repository

To initialize a new Git repository.

```sh
git init
```

## Cloning a Repository

To clone an existing repository.

```sh
git clone https://github.com/user/repository.git
```

Replace `https://github.com/user/repository.git` with the URL of the repository you want to clone.

## Checking Repository Status

To check the status of the working directory and staging area.

```sh
git status
```

## Adding Files to Staging Area

To add a file to the staging area.

```sh
git add file-name
```

To add all files to the staging area.

```sh
git add .
```

Replace `file-name` with the name of the file you want to add.

## Committing Changes

To commit changes with a message.

```sh
git commit -m "commit message"
```

Replace `commit message` with your commit message.

## Viewing Commit History

To view the commit history.

```sh
git log
```

## Creating a Branch

To create a new branch.

```sh
git branch branch-name
```

Replace `branch-name` with the name of the branch you want to create.

## Switching Branches

To switch to another branch.

```sh
git checkout branch-name
```

Replace `branch-name` with the name of the branch you want to switch to.

## Merging Branches

To merge a branch into the current branch.

```sh
git merge branch-name
```

Replace `branch-name` with the name of the branch you want to merge.

## Pushing Changes to Remote

To push changes to a remote repository.

```sh
git push origin branch-name
```

Replace `branch-name` with the name of the branch you want to push.

## Pulling Changes from Remote

To pull changes from a remote repository.

```sh
git pull origin branch-name
```

Replace `branch-name` with the name of the branch you want to pull.

## Fetching Changes from Remote

To fetch changes from a remote repository.

```sh
git fetch origin
```

## Reverting Changes

To revert a commit by creating a new commit.

```sh
git revert commit-id
```

Replace `commit-id` with the ID of the commit you want to revert.

## Stashing Changes

To stash changes in the working directory.

```sh
git stash
```

## Applying Stashed Changes

To apply stashed changes.

```sh
git stash apply
```

## Deleting a Branch

To delete a local branch.

```sh
git branch -d branch-name
```

To delete a remote branch.

```sh
git push origin --delete branch-name
```

Replace `branch-name` with the name of the branch you want to delete.

## Viewing Remote Repositories

To view remote repositories.

```sh
git remote -v
```

## Adding a Remote Repository

To add a remote repository.

```sh
git remote add origin https://github.com/user/repository.git
```

Replace `https://github.com/user/repository.git` with the URL of the remote repository you want to add.

## Removing a Remote Repository

To remove a remote repository.

```sh
git remote remove origin
```

Replace `origin` with the name of the remote repository you want to remove.
