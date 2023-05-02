# 遇到的问题

## git错误 error: failed to push some refs to 'https://github

[(92条消息) 解决办法：git错误 error: failed to push some refs to 'https://github.com/..._米汤就是稀饭的博客-CSDN博客](https://blog.csdn.net/qq_30152625/article/details/90404727)

## 撤销修改

[(92条消息) Git撤销修改_git 撤销修改_路痴的兔子的博客-CSDN博客](https://blog.csdn.net/qq_37284607/article/details/118822368)

[(92条消息) git如何撤销工作区的修改_git撤销工作区修改_寅鸷的博客-CSDN博客](https://blog.csdn.net/Zx13170918986/article/details/120838397)

[Git 之 reset --hard 回退/回滚到之前的版本代码后，后悔了，如何在恢复之后的版本的方法简单整理_git reset后怎么恢复_仙魁XAN的博客-CSDN博客](https://blog.csdn.net/u014361280/article/details/127740356)

## 比较差异

[Git 基本命令 -- 你用过 git diff 吗？补习一下吧 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/148312377)

[(92条消息) Git版本控制管理——diff_git diff 指定文件_止步听风的博客-CSDN博客](https://blog.csdn.net/SAKURASANN/article/details/125472567)

## 删除

git rm "filename.txt" 这个命令执行后是暂存区和工作区同步删除，没有commit到本地版本库；要撤回暂存区和工作区的删除操作分为两步：

- 撤回从本地删除操作被add到暂存区的操作 git reset

​	<img src=".//images//image-20230502170148512.png" alt="image-20230502170148512" style="zoom:67%;" /> <img src=".//images//image-20230502170342215.png" alt="image-20230502170342215" style="zoom:67%;" />

- 撤回本地删除操作 git checkout -- "filename.txt"

<img src=".//images//image-20230502170515563.png" alt="image-20230502170515563" style="zoom:67%;" /> <img src=".//images//image-20230502170651229.png" alt="image-20230502170651229" style="zoom:67%;" />

或者直接工作区和暂存区同时回退到版本库中上一次commit的状态 git reset --hard HEAD

<img src=".//images//image-20230502170820169.png" alt="image-20230502170820169" style="zoom:67%;" /> <img src=".//images//image-20230502170831107.png" alt="image-20230502170831107" style="zoom: 50%;" />

## 分支管理与远程仓库

[(92条消息) git push origin master和git push的区别_公孙元二的博客-CSDN博客](https://blog.csdn.net/Amnesiac666/article/details/120511618)

##### 1.git push <repository> <localbranchName>:<branchName>

  repository 为远程主机地址，将本地指定分支推送到远程指定分支。

##### 2.git push origin master

  将本地的 master 分支推送到远程的 master 分支。

##### 3.git push origin :master

  删除远程 master 分支，当省略本地分支名时，效果等同于删除远程此分支。

##### 4.git push origin

  将当前分支推送到 origin 主机的对应分支。

##### 5.git push

  进行默认推送。

##### 6.git push origin --delete <branchName>

  删除远程某个分支。

##### 7.git push --all origin

  将本地所有分支都推送到 origin 主机。

#### git log命令

[(92条消息) git 之 git log命令原来还能这么玩_Z_ One Dream的博客-CSDN博客](https://blog.csdn.net/weixin_42335036/article/details/122974672)

#### git-merge简介

[git merge 的三种情况 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/545635048)

git-merge命令是用于从指定的commit(s)合并到当前分支的操作。

> 注：这里的指定commit(s)是指从这些历史commit节点开始，一直到当前分开的时候。

git-merge命令有以下两种用途：

1. 用于git-pull中，来整合另一代码仓库中的变化（即：git pull = git fetch + git merge）
2. 用于从一个分支到另一个分支的合并

假设下面的历史节点存在，并且当前所在的分支为“master”：

![img](https:////upload-images.jianshu.io/upload_images/1226129-bce91fe9c75175ad.png?imageMogr2/auto-orient/strip|imageView2/2/w/209/format/webp)


 那么`git merge topic`命令将会把在master分支上二者共同的节点（E节点）之后分离的节点（即topic分支的A B C节点）重现在master分支上，直到topic分支当前的commit节点（C节点），并位于master分支的顶部。并且沿着master分支和topic分支创建一个记录合并结果的新节点，该节点带有用户描述合并变化的信息。



> 即下图中的H节点，C节点和G节点都是H节点的父节点。

![img](https:////upload-images.jianshu.io/upload_images/1226129-0fcb16bd7f842832.png?imageMogr2/auto-orient/strip|imageView2/2/w/236/format/webp)

作者：Chuckiefan
链接：https://www.jianshu.com/p/58a166f24c81
来源：简书

#### merge合并冲突到底什么时候会发生

[git merge 的三种情况 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/545635048)

[(19 封私信 / 8 条消息) Git到底什么情况下会产生合并冲突？ - 知乎 (zhihu.com)](https://www.zhihu.com/question/510309450/answer/2342052525?utm_id=0)

#### git push

[git创建本地与远程分支的同步与合并 - 掘金 (juejin.cn)](https://juejin.cn/post/6844903713803337741)[git创建本地与远程分支的同步与合并 - 掘金 (juejin.cn)](https://juejin.cn/post/6844903713803337741)

#### git fetch、merge、pull 

[(92条消息) git 远程分支与本地分支_本地分支和远程分支_滨边美波她男友的博客-CSDN博客](https://blog.csdn.net/weixin_42109053/article/details/127475184)
