#### A Visual Guide to Version Control  //版本控制
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

## Checkins

![image](https://user-images.githubusercontent.com/31954987/196017294-73661a15-bdab-4908-a224-8fd3c5eadee1.png)
each time we check in a new version, we get a new revision(r1, r2, r3, etc.). In Subversion you'd do:
> ```
> Zihan add list.txt
> (modify the file)
> zihan ci list.txt -m "Changed the list"
> ```

The `-m` flag is the message to use for this checkin.

## Checkouts and Editing 结账与编辑
in reality, **check out, edit and check in** 

![image](https://user-images.githubusercontent.com/31954987/196017929-282c342e-267b-44e8-baf3-f3e5224b8c11.png)
> ```
> zihan co list.txt (get latest version)
> ...edit file...
> zihan revert list.txt (throw away changes)
> zihan co -r2 list.txt (check out particular version)
> ```



#### Intro to Distributed Version Control  //分布式版本控制
#### Aha! Moments When Learning Git  //学习Git时的 Aha! Moments
