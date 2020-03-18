---
title: 分布式版本控制Git
date: 2020-03-18 14:10:14
tags:
- 工具
categories:
- 工具
index_img: https://i.loli.net/2020/03/18/y1SbEo2Hn3mNeqs.jpg
banner_img:
---

Git是目前世界上最先进的分布式版本控制系统（没有之一）。

# 常用命令

```bash
$ git init #初始化
$ git add . #添加全部到仓库,实际上就是把文件修改添加到暂存区
$ git commit -m "message" #提交信息,实际上就是把暂存区的所有内容提交到当前分支
$ git status #查看仓库状态
$ git diff file #查看文件修改内容
$ git log #查看历史记录
$ git reset --hard HEAD^ #回退版本
$ git reflog #查看回退记录
$ git checkout -- file #把文件在工作区的修改全部撤销
$ git rm file #删除一个文件
```

# 工作区和暂存区

工作区就是你在电脑里能看到的目录，工作区有一个隐藏目录`.git`，这个不算工作区，而是Git的版本库。Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支`master`，以及指向`master`的一个指针叫`HEAD`。

# 远程仓库

```bash
$ git remote add origin URL #添加远程仓库,远程库的名字就是origin
$ git push -u origin master #把本地库master的内容推送到远程origin
$ git clone URL #克隆远程到本地
```

# 分支

```bash
$ git checkout -b dev #创建并切换到分支dev
$ git checkout dev #切换到分支dev
$ git branch #查看分支
$ git merge dev #合并分支到当前
$ git branch -d dev #删除分支 -D强制
$ git switch -c dev #创建并切换到分支dev,新命令与checkout区分
$ git stash #把当前工作现场“储藏”起来，等以后恢复现场后继续工作：
$ git stash apply #恢复不删除
$ git stash drop #来删除
$ git stash pop #恢复的同时把stash内容也删了
$ git stash list #查看
$ git cherry-pick <commit> #把另外分支提交的修改“复制”到当前分支
```

