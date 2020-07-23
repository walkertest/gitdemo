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



```

## 删除分支
```
删除本地的某个分支
git branch -d branchName/git branch -d branchName(强制删除)


删除远程分支，并将其它分支修改为master
在gitlab/github上，将默认分支 修改为 你想提升为master的那个分支A，然后删除master分支，删除完成之后，从分支A上创建一个master分支，再将默认分支修改为master即可. 然后删除分支A.

```

## 如何回滚代码
```
git reset commmitid;   (git reset --hard commitid 是直接回退到指定的commit，将commitid之后的相关变更直接丢弃掉.)
git push -f 


git revert commitid,是指的回退指定的commitid（生成一个新的commit来回退这个变更）--将本次的commit去掉.
git revert test2
git revert test  //测试.
```


## 如何合并提交记录
在分支上提交很多次的代码，如何将代码记录合并.

## 如何设置更新github主仓库代码
参考帖子：https://blog.csdn.net/yaya1943/article/details/54582530
```
git remote add tarsOrigin https://github.com/TarsCloud/TarsJava.git
git remote -v
git pull tarsOrigin master
git push
然后做通过github提交merge request即可.
```


## tag相关操作
```
git tag，查看当前的tag
git tag -a tagname -m "comment" ,创建一个tag
git push origin tagname,将tagpush到远程仓库.
git checkout commitid -b newBranch ，基本某个tag的commitid，拉取新的分支.
```

## FAQ
### unable to update local ref
参考：https://cloud.tencent.com/developer/ask/37468
删除掉本地提示报错的那个文件就好了，可能是相同的文件名或者大小写导致的.
