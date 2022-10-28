## There's a staging area! //暂存区
#### Git has a staging area. **Git has a staging area!!!** //Git 暂存区
#### There's both a repo("object database") and a staging area(so called "index").Checkins have two steps: //对象数据库，暂存区；Checkins 包含两个步骤
- `git add foo.txt`
  - Add foo.txt to the index. it is not checked in yet!

- `git commit -m "message"`
  - Put staged files in the repo; they're now tracked
  - You can "`git add -update`" to stage all tracked, modified files

#### **Why stage?** Git's flexible: if a, b and c are changed, you can commit them separately or together. //分开或者共同commit

#### But now there's two undos: //两种undos
- `git checkout foo.txt`
  - Undo local changes (like svn revert) //Undo本地改变

- `git reset HEAD foo.txt`
  - Remove from staging area(local copy still modified) //从暂存区移除

#### Add and commit, add and commit -- Git has a rhythm. //git 的节奏

## Branching is "Save as..." //暂存区

#### Branches are like "Save as..." on a directory. Best of all:
- Easily merge changes with the original(changes tracked and never applied twice) // 汇合改变到 原始
- No wasted space (common files only stored once)

#### In practice, svn is like a single shared drive, where you can only revert to one bakcup

## Imagine virtual directories //想象一个虚拟目录
#### I see branches as "virtual directories" in the .gif folder. While inside a physical directory (c:\project or ~/project), you traverse virtual directories with a checkout.

- `git checkout master`
  - switch to master branch("cd master")

- `git branch dev`
  - create new branch from existing ("cp * dev")
  - you still need to "cd" with "git checkout dev"

- `git merge dev`
  - (when in master) pull in changes from dev("cp dev/* .") 
- `git branch`
  - list all branches("ls")

#### "change to dev directory(checkout)... "
#### "make changes..."
#### "save changes (add/commit)..."
#### "change to master directory ..."
#### "copy in changes from dev (merge)"
#### The physical directory is a scratchpad. Virtual directories are affected by git commands:

- `rm foo.txt`
  - Remove foo.txt from your sandbox(restored if you checkout the branch again) //从沙盒中移除 foo.txt
- `git rm foo.txt`
  - Remove foo.txt from current virtual directory //从现有虚拟目录中移除 foo.txt
  - Gotcha: you need to commit that change! //

## Know the current branch //当前的分支
#### Just like seeing your current directory, put the current branch in your prompt!
#### in my .bash_profile:
> ```
> parse_git_branch() {
>    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* (.*)/(1)/'
> }
> 
> export PS1="[33[00m]u@h[33[01;34m] W [33[31m]$(parse_git_branch) [33[00m]$[33[00m] "
> ```

## Visualize your branch structure //可视化分支结构
#### Git leaves branch organization to you. Nvie.com has a great branch strategy 
![image](https://user-images.githubusercontent.com/31954987/198338204-fc85b7fc-c12b-4d1a-880e-17d3b4b8889d.png)
- Have a mainline(master). Mentally it's on the far right. //心智模型中的右侧🫱，为主线分支
- Create branches(master -> dev) and subbranches (dev -> featureX) the further from master, the crazier //创建分支 与分分支
- Only merge with neighbors (master -> dev -> feature X, or featureX -> dev -> master) //

#### stay sane by choosing a branch layout up front. I have a master tracking a svn project, and dev for my own code. In general, master is clean so I can branch anytime for one-off fixes.


## understand local VS. remote //本地与远程
#### Git has local and remote commands; Work locally, syncing remotely as needed.

### Local data //本地数据
- `git init`
  - create local repo
  - use git add/commit/branch to work locally

### Remote data //远程数据
- `git remote add name path-to-repo`
  - track a remote repo(usually "origin" from an existing repo) //追踪远程repo
  - remote branches are "origin/master", "origin/dev" etc.

- `git branch -a`
  - list all branches(remote and local) //罗列所有分支（包括本地与远程）

- `git clone path-to-repo`
  - create a new local git repo copied from a remote one
  - local master tracks remote master //本地master追踪 远程master

- `git pull`
  - merge changes from tracked remote branch (if in dev, pull from origin/dev) //从追踪的远程分支合并变化 
- `git push`
  - send change to tracked remote branch (if in dev, push to origin/dev)

### **Why local and remote?** Subversion has central checkins, you avoid committing unfinished work. With git, local commits are frequent and you only push when ready. //避免commit 未完成的工作，本地commits是常用的，you only push当需要。

##GUIDs are GOOD

