# cmd

<!-- create time: 2015-08-30 14:32:43  -->

<!-- This file is created from $MARBOO_HOME/.media/starts/default.md
本文件由 $MARBOO_HOME/.media/starts/default.md 复制而来 -->

```shell
git add --把文件添加进去，实际上就是把文件修改添加到暂存区

git commit --提交更改，实际上就是把暂存区的所有内容提交到当前分支。

git checkout -b mybranch origin/mybranch --从远程分支克隆到本地并切换到该分支

git branch mybranch

git checkout HEAD . 

git checkout -- readme.txt 
命令中的--很重要，没有--，就变成了“切换到另一个分支”的命令
意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

git reset . 

git reset --hard HEAD 
--可取消merge HEAD指当前版本  
上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。
注意同mixed的区别
hard会回到某个版本的稳定状态。mixed会让这个版本后的修改保留，可以使用 add  commit 操作去提交

git push origin --delete branchName --删除远程分支

git branch -D branchName --删除本地分支

git log --pretty=oneline --只打印版本号

git reflog --显示历史操作 可以通过这找回数据

```
