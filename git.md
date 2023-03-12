# Git

## Basic Commands

### Clone A Repository

```sh
$ git clone <repository_url>`
```

### Create New Repository Procedure

Firstly, create a repository on Github and get *your_repo_url*. Secondly, go to your local project directory and initialize *git*:

```sh
$ git init
$ git add README.md
$ git status
$ git add <file1> <file2> ...
$ git rm <file1> <file2> ...
$ git status
$ git commit -m "your_comment"
# 'origin' means the remote end of your repository
$ git remote add origin <your_repo_url>
# use '-u' for the first time, it can be ignored afterwards
$ git push -u origin <master_or_other_branch>
```

### Discard Working Directory Changes

```sh
$ git checkout -- <file1> ...
```

### Unstage Changes to Working Directory

```sh
$ git reset HEAD <file1> ...
```

### Undo a Local Commit

```sh
$ git reset HEAD~1
```

### Show Logs and History

```sh
# show current HEAD and its ancestry
$ git log --oneline
# draw graph of branch structure
$ git log --graph --pretty=oneline --abbrev-commit
# shows the entire history
$ git reflog
```

### Reset to A Version

```sh
# where commit_id can be found in the log/history
$ git reset --hard <commit_id>
```

### Branch

```sh
# show a list of both local and remote branches
$ git branch -a
# create a local branch from a remote branch
$ git checkout -b <new_local_branch> <remote_branch>
# checkout or switch to an existing branch
$ git checkout <branch_name>
$ git merge <branch_name>
# delete a branch
$ git branch -d <branch_name>
```

### Remote Info

```sh
$ git remote -v
# check if the branch gets updated
$ git remote -v update
# show the original information of the cloned repository
$ git remote show origin
```

### Work Collaboration Procedure

```sh
$ git push origin <branch_name>
$ git pull
$ git branch --set-upstream <branch_name> <origin/branch_name>
```

### Tag

```sh
# default will tag HEAD
$ git tag <tag_name>
$ git tag <tag_name> <commit_id>
# show tag list
$ git tag
# add tag message
$ git tag -a <tag_name> -m "your tag message" <commit_id>
# show tag information
$ git show <tag_name>
$ git push origin <tag_name>
$ git push --tag
```

### Diff

```sh
# show diff of the file that hasn't been git-added
$ git diff file
# show diff of the added file
$ git diff --cached file
```

### Update Remote Changes

```sh
# update all local branches set to track remotes ones, but not merge any changes in
$ git remote update
# update the branch currently you're on, but not merge any changes in
$ git fetch
# update AND merge the remote changes to your current branch
$ git pull
```

### Procedure of Syncing a Fork

```sh
# check if upstream is set correctly
$ git remote -v
# fetch changes on the upstream
$ git fetch upstream
# switch to your branch
$ git checkout <your_branch>
# merge the changes to your branch
$ git merge upstream/<your_branch>
$ git status
$ git branch -a
# push the merged local changes to your fork
$ git push origin <your_branch>
```

### Save Unfinished Work

```sh
# save staged and unstaged changes in the stash stack, undoing thing to the latest commit
$ git stash
# stash including untracked files
$ git stash -u or $ git stash --include-untracked
# show all the stashes
$ git stash list
# show stash reference 1 in patch format
$ git stash show stash@{1} -p
# apply the latest stash on current branch and stash is removed from stack
$ git stash pop
# apply the stash reference 3 on current branch and stash remains in the stack
$ git stash apply stash@{3}
# clear all stashes
$ git stash clear
# delete stash reference 2
$ git stash drop stash@{2}
```

## Useful Configs

1. Graphical view of branches
Add the following alias to the ~/.gitconfig, and running `git log1` or `git log2` will output a clear view of the relationship of branches.

```sh
[alias]
log1 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
log2 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''%C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all
```

## Branching Model

master (production) - hotfixes - releases - develop - features

## Reference

[https://git-scm.com/docs](https://git-scm.com/docs)

[A Beginner's Git and GitHub Tutorial](https://blog.udacity.com/2015/06/a-beginners-git-github-tutorial.html)

[Git - Simple Guide](http://rogerdudler.github.io/git-guide/)

[Xuefeng Liao's Git Tutorial](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

[Atlassian Git Cheatsheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

[Git Branching Model](https://nvie.com/posts/a-successful-git-branching-model/)
