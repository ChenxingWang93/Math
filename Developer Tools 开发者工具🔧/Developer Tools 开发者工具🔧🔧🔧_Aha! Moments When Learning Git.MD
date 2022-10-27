## There's a staging area! //暂存区
#### Git has a staging area. **Git has a staging area!!!**
#### There's both a repo("object database") and a staging area(so called "index").Checkins have two steps: //Checkins 包含两个步骤
- `git add foo.txt`
  - Add foo.txt to the index. it is not checked in yet!

- `git commit -m "message"`
  - Put staged files in the repo; they're now tracked
  - You can "`git add -update`" to stage all tracked, modified files

#### **Why stage?** Git's flexible: if a, b and c are changed, you can commit them separately or together.

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

## Imagine virtual directories
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
  - Remove foo.txt from your sandbox(restored if you checkout the branch again)
- `git rm foo.txt`
  - Remove foo.txt from current virtual directory 
  - Gotcha: you need to commit that change!

## Know the current branch
#### Just like seeing your current directory, put the current branch in your prompt!
#### in my .bash_profile:
- ```
- 
- ```
