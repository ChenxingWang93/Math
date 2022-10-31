# A Visual Guide to Version Control  //版本控制
![image](https://user-images.githubusercontent.com/31954987/196000722-4ca79f73-3dc3-44e1-beac-3083f33e5cbe.png)

#### Version Control track your files over time, when you mess up you can easily get back to a previous working version.
**you’ve probably cooked up** your own version control system without realizing it had such a geeky name, Got any files like this?
- 3D打印与航天白皮书1.0_3D科学谷.pdf
- 3D打印与航天白皮书第二版_3D科学谷(1).pdf
<img width="870" alt="Screen Shot 2022-10-16 at 03 48 54" src="https://user-images.githubusercontent.com/31954987/196005197-daddae57-3436-4203-a9d5-9cddd5242608.png">

**It's why we use "Save as"** you want the new file without obliterating the old one. It's a common problem, and solutions are usually like this:
- Make a **single backup copy** (Document.old.txt)
- Add **version number or date** (Document_V1.txt),(DocumentMarch2015.txt)
- **shared folder**

### Why Do We Need a Version Control System (VCS)? 为什么需要一个版本控制系统？
shared folder/naming system is fine for class projects or one - time papers. but software projects? NOT A CHANCE

Large, fast - changing projects with many authors need a Version Control System(geekspeak for "file database") to track changes and avoid general chaos.
a good VCS does the following:
- **Backup and Restore**: 备份与还原
- **Synchronization**:  同步
- **Short-term undo**:  短期撤销
- **Long-term undo**: 长期撤销
- **Track Changes**:  追踪变化
- **Track Ownership**:  追踪所有权
- **Sandboxing**: 
- **Branching and merging**:  分支与合并

### Learn the Lingo 学行话
Most VCS involve the following concepts,
## Basic Setup 基本设置
- **Repository(repo)**: The database storing the files 存储📃的数据库
- **Server**: The computer storing the repo 存储repo的💻
- **Client**: The computer connecting to the repo 连接到💻的repo 
- **Working Set/ Working Copy**: local directory of files, where you make changes 本地文件
- **Trunk/Main**: The primary location for code in the repo. Think of code as a family tree - the trunk is the main line 树干是主枝 

## Basic Actions 基本行动
- **Add**: Put a 📃 into the repo for the first time, begin tracking it with Version Control 
- **Revision**: What version a file is on(v1,v2,v3,etc) 📃文件版本
- **Head**: The latest version in the repo 仓库里最近的版本
- **Check out**: Download a file from the repo 仓库中⏬📃
- **Check in**: ⬆️📃 to the repository(if it has changed).The file get a new version number, and people can "check out" the latest one.
- **Checkin Message**:  A short message describing what has changed. 描述改变了什么
- **Changelog/History**:  A list of changes made to a file since it was created 文件中的改变
- **Update/Sync**:  Synchronize your files with the latest from the repository. this lets you grab the latest revisions of all files 同步最近📃，抓取最近的修订
- **Revert**: throw away your local changes and reload the latest version from the repo 扔掉本地改变重载最新版本

## Advanced Actions 高级行动

- **Branch**：分支；Create a separate copy of a file/ folder for private use (bug fixing, testing, etc) Branch 作为动词("branch the code") 作为动词("Which branch is in it?")
- **Diff/Change/Delta**: 变化/ 修改 /Finding the differences between two files. Useful for seeing what changed between revisions 找2⃣️📃不同
- **Merge (or patch)**: 合并（或补丁）
- **Conflict**: 冲突
- **Resolve**:  解决
- **Locking**:  锁定
- **Breaking the lock**:  解锁
- **Check out for edit**: 

And a typical scenario goes like this:
张梓焓 **add** a file (`list.txt`) to the **repo**. **checks it out**, makes a change("")

## Checkins 签入

![image](https://user-images.githubusercontent.com/31954987/196017294-73661a15-bdab-4908-a224-8fd3c5eadee1.png)
#### each time we check in a new version, we get a new revision(r1, r2, r3, etc.). In Subversion you'd do:
> ```
> svn add list.txt
> (modify the file)
> svn ci list.txt -m "Changed the list"
> ```

The `-m` flag is the message to use for this checkin.

## Checkouts and Editing 查看与编辑
#### in reality, **check out, edit and check in** 循环♻️是高频操作

![image](https://user-images.githubusercontent.com/31954987/196017929-282c342e-267b-44e8-baf3-f3e5224b8c11.png)
#### if you don't like your changes and want to start over, you can **revert**恢复 to the previous version and start again(or stop), when checking out,(查看) you get the latest revision by default. you can also specify a particular revision. 
> ```
> svn co list.txt (get latest version)
> ...edit file...
> svn revert list.txt (throw away changes)
> svn co -r2 list.txt (check out particular version)
> ```
🌟SVN means Subversion

## Diffs 变化
![image](https://user-images.githubusercontent.com/31954987/196030198-77f4c5fe-977d-4bea-9871-9cc00f6b6a08.png)

#### from r1 to r2: add eggs(+Eggs)
#### from r2 to r3: add Juice(+Juice)
#### from r3 to r4: remove Juice add Soup(-Juice, +Soup)
#### Most VCS **store diffs rather than full copies of the file** //存储不同的部分而不是两份完全不同的📃
#### this saves disk space: 4 revisions of a file means 1 copy 4 small diffs 

#### In SVN, we diff two revisions of a file like this:
> ```
> svn diff -r3:4 list.txt
> ```

#### Diffs help us notice changes ("How did you fix that bug again?") and even apply them from one branch to another 
> ```
> +Eggs
> +Soup
> ```

#### Notice how "Juice" wasn’t even involved - the direct jump from r1 to r4 doesn’t need that change, since Juice was overridden by Soup.

## Branching //分支
#### branches let us copy code into a separate folder so we can monkey with it separately: //分支允许复制代码到独立的文件夹

![image](https://user-images.githubusercontent.com/31954987/199008359-c657f2de-6158-43c4-a9cf-04d191bab203.png)

#### In Subversion, you create a branch simply by copying a directory to another.
> ```
> svn copy http://path/to/trunk http://path/to/branch
> ```


## Mergin //合并代码
#### we only want to apply the changes **that happened in the branch** that means we diff r5 and r6, and apply that to the main trunk:
![image](https://user-images.githubusercontent.com/31954987/199009415-35767a18-ce4a-400b-bcf2-f2f8a9404b61.png)
#### if we diffed r6 and r7, we would lose the "Bread" feature that was in main. This is a sublet point - imagine "peeling off" the changes from the experimental branch(+Rice) and adding that to main. Main may have had other changes, which is ok -  we just want to insert the Rice feature.

#### In Subversion, merging is very close to diffing. Inside the main trunk, run the command:
> ```
> svn merge -r5:6 http://path/to/branch
> ```

#### This command diffs r5-r6 in the experimental branch and applies it to the current location. Unfortunately, Subversion doesn’t have an easy way to keep track of what merges have been applied, so if you’re not careful you may apply the same changes twice. It’s a planned feature, but the current advice is to keep a changelog message reminding you that you’ve already merged r5-r6 into main. 

## Conflicts
#### Many times, the VCS can automatically merge changes to different parts of a file. Conflicts can arise when changes appear that don’t gel: Joe wants to remove eggs and replace it with cheese (-eggs, +cheese), and Sue wants to replace eggs with a hot dog (-eggs, +hot dog).


![image](https://user-images.githubusercontent.com/31954987/199011190-bf69aae7-3097-486c-b614-7fd04a3a6c32.png)
#### at this point it's a race: if Joe checks in first, that's the change that goes through(and Sue can't make her change)

#### When changes overlap and contradict like this, the VCS may report a **conflict** and not let you check in — it’s up to you to check in a newer version that **resolves** this dilemma. A few approaches:

- **Re-apply your changes**. Sync to the the latest version (r4) and re-apply your changes to this file: Add hot dog to the list that already has cheese.
- **Override their changes with yours**. Check out the latest version (r4), copy over your version, and check your version in. In effect, this removes cheese and replaces it with hot dog.

#### Conflicts are infrequent but can be a pain. Usually I update to the latest and re-apply my changes. //冲突不常发生，但会很痛苦，通常我会更新到最近的版本，然后重新-应用我的改变

## Tagging //🏷️
#### Who would have thought a version control system would be Web 2.0 compliant? Many systems let you tag (label) any revision for easy reference. This way you can refer to “Release 1.0” instead of a particular build number: //vcs会顺从web2.0，很多系统允许你贴🏷️作为参考，这个方法你可以退回“release 1.0”

![image](https://user-images.githubusercontent.com/31954987/199013898-9b9dd052-ba7f-41c1-9727-1f1db2b43198.png)

#### in subversion, tags are just branches that you agree not to edit; they are around for posterity, so you can see exactly what your version 1.0 release contained. Hence they end in a stub — there’s nowhere to go.
> ```
> (in trunk)
> svn copy http://path/to/revision http://path/to/tag
> ```

## Real-life example: Managing Windows Source Code //管理windows 源代码
#### We guessed that Windows was managed out of a shared folder, but it’s not the case.//我们以为Windows 通过分享文件夹，当事实却并非如此
#### https://learn.microsoft.com/en-us/archive/blogs/larryosterman/
- There’s a main line with stable builds of Windows. //有稳定的主线
- Each group (Networking, User Interface, Media Player, etc.) **has its own branch** to develop new features. These are under development and less stable than main. //每个小组（networking、ui、media player）都有自己的分支来开发新功能。比主分支更不稳定一些
#### You develop new features in your branch and “Reverse Integrate (RI)” to get them into Main. Later, you “Forward Integrate” to bring the latest changes from Main into your branch: //开发新功能，然后反植入，随后向前植入 从主线到分支带来最新的变化
![image](https://user-images.githubusercontent.com/31954987/199016545-dd2fa89f-4f20-46a1-9e1b-22830b33dc98.png)

#### In reality, there’s many layers of branches and sub-branches, along with quality metrics that determine when you get to RI. But you get the idea: branches help manage complexity. Now you know the basics of how one of the largest software projects is organized. //很多层的分支与子分支，根据不同的质量矩阵来确定什么时候反向植入，但是总而言之通过分支的方式帮助管理复杂和大型的软件开发项目，让它们的开发过程变得井井有条。

## key takeaways //重要的

- **Use version control**. Seriously, it’s a good thing, even if you’re not writing an OS. It’s worth it for backups alone.
- **Take it slow**. I’m only now looking into branching and merging for my projects. Just get a handle on using version control and go from there. If you’re a small project, branching/merging may not be an issue. Large projects often have experienced maintainers who keep track of the branches and patches.
- Keep Learning. There’s plenty of guides for SVN, CVS, RCS, Git, Perforce or whatever system you’re using. The important thing is to know the concepts and realize every system has its own lingo and philosophy. Eric Sink has a detailed version control guide also.


