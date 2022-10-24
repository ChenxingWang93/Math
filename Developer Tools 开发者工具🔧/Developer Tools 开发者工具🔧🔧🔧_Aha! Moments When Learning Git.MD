## There's a staging area! //暂存区
### Git has a staging area. **Git has a staging area!!!**
### There's both a repo("object database") and a staging area(so called "index").Checkins have two steps: //Checkins 包含两个步骤
- `git add foo.txt`
  - Add foo.txt to the index. it is not checked in yet!

- `git commit -m "message"`
  - Put staged files in the repo; they're now tracked
  - You can "`git add -update`" to stage all tracked, modified files

### **Why stage?** Git's flexible: if a, b and c are changed, you can commit them separately or together.

### But now there's two undos: //两种undos
- `git checkout foo.txt`
  - Undo local changes (like svn revert) //Undo本地改变

- `git reset HEAD foo.txt`
  - Remove from staging area(local copy still modified) //从暂存区移除

### Add and commit, add and commit -- Git has a rhythm. //git 的节奏
