# Git - Working with Branches

## List branches

List local branches:

```
git branch
```

List local and remote branches: 

```
git branch -a
```

List remote branches: 

```
git branch -r
```

## Create and switch branches (using switch, with Git v. 2.23 or higher)

Create a branch and switch to it:

```
git switch <branch-name-without-origin>
```

If this branch already exists locally, git will switch to it.

If this branch does not yet exist locally, it will try to find a remote branch that could fit, check it out, create a local tracking branch and switch to the new branch.

*Note:* This works fine, with only one remote and when the remote branch has the same name.

Example:
```
$ git branch -a
* main
  remotes/origin/feature/annas-new-feature
  remotes/origin/main

$ git switch feature/annas-new-feature
```

Change to a branch:

```
git switch <branch-name>
```

## Create and switch branches (using checkout, prior to Git v. 2.23)

Create a branch and switch to it:

```
git checkout -b <branch-name>
```

Change to a branch:

```
git checkout <branch-name>
```

## Delete branches

Delete a local branch:

```
git branch -d <branch-name>
```

Delete a local and remote branch: (see https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches)

```
git fetch --all --prune           # to make sure, your branches are up to date
git branch -a                     # list all branches
git branch -dr <branch-name>      # delete branch and remote branch
```

Delete a remote branch:

```
git push origin --delete <branch-name>
```
