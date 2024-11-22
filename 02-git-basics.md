# Git - Basic commands


## Clone a repository

* cd to the directory for your workspaces. Note the default command, will create a folder with the name of your repository.

```
cd /folder/where/my/repositories/are
git clone <url> [folder-for-this-repository]
```

References
* [git-scm.com/docs/git-clone](https://git-scm.com/docs/git-clone)
* [Git Book - 2.1 Git Basics - Getting a Git Repository](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)


## Status, add files, commit and push changes

* to see what has changed, use `git status`.
* add changes with `git add <filename>`. See [git-scm.com/docs/git-add](https://git-scm.com/docs/git-add)
* commit changes with a message. See [git-scm.com/docs/git-commit](https://git-scm.com/docs/git-commit)

```
git commit -m "commit message"
```

* push changes with `git push`


### Reset uncommitted adds

If you added some files, but do not want to commit them after all, use `git reset <filename>` or `git reset` to reset all added files.

```
git reset <filename>
```

## Undo (restore) local changes

*Warning:* Cannot be reverted!

If you have changed a file locally, but do not want to commit it, instead you want to reset it to the previous state.

```
git restore <filename>
```

### Amend the most recent commit

To add something to your last commit, use `git commit --amend`.
