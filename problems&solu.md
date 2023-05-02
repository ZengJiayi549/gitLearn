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

<img src=".//images//image-20230502170820169.png" alt="image-20230502170820169" style="zoom:67%;" /> <img src=".//images//image-20230502170831107.png" alt="image-20230502170831107" style="zoom:67%;" />

