# 丢弃掉本地的提交
```
git checkout . #本地所有修改的。没有的提交的，都返回到原来的状态
git stash #把所有没有提交的修改暂存到stash里面。可用git stash pop回复。
```


# 如何回退已经在远程仓库的某几次提交


# 分支操作
## 查看远程分支
```
查看远程仓库地址：
git remote -v

查看本地分支对应的远程分支:
git branch -vv
如果没有显示远程分支，那么可能是从本地的某个分支拉出来的分支


删除本地的某个分支
git branch -d branchName/git branch -d branchName(强制删除)
```
