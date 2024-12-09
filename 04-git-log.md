# Git - Displaying the History with Log

## Display the History

The basic 'git log' command, lists the most recent change first. It displays the hash, author, date, message and branches. The display is continuous as in 'more', you use space to show the next page and q to quit the history.

```
git log
# use space to load the next page
# use q to quit
```

Simple way to have only one line per commit:

```
git log --oneline
```

Simple way to get only a fixed number of commits:

```
git log -10
```

They may be combined:

```
git log --oneline -10
```

The history display is very customizable. This is my current favourite commaand:

```
git log --pretty=format:"%h %an %ah >%Cgreen%d%Creset %s" -20
```

## Links

* Good overview on displaying git history: https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History
* Full manual page on the git log command: https://git-scm.com/docs/git-log
