#以下是git的教程
git add 
git commit -m "-m后面跟着变更说明"

git status   查看修改了但是没有commit的文件
git diff 查看了没有commit的部分与之前文件的不同之处

git log  查看从近到远的历史修改日志 
参数 --pretty=oneline

git reset --hard HEAD^       回滚到上一版本 
git reset --hard 2f40632fb1942badd6a31a976  也可以

HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本 

git diff HEAD -- readme.txt 可以查看工作区和最新版本的区别

命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
--很重要，没有--，就变成了“切换到另一个分支”的命令，

git reset HEAD file
把暂存区的文件清除


