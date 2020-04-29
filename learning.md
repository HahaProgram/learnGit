##学习git
###查看那些文件没有添加到暂存区
git status
###添加到暂存区
####git add . / git add -u / git add -a 的区别
git add .  将所有发生变化的文件添加到暂存区
git add -u   监控已经添加到暂存区的文件，进行提交
git add -a 是上面两个功能的合集
###将提交暂存区的文件提交到正式仓库
####git commit -m "massage" / git commit -a -m "massage" / git commit --amend
git commit -m "massage" :-m 表示添加信息
git commit -a -m "massage" -a -m： git add 和 git commit -m 的合集
###查看操作日记本
git log
###查看执行命令记录
git reflog
···$ git reflog
b921ea3 (HEAD -> master) HEAD@{0}: commit: 小白测试
6b5fbaa HEAD@{1}: commit: 小白再进10吨货物
8b98ec7 HEAD@{2}: commit (initial): 小白货物进厂 10吨
###版本回退到上一个版本
git reset --hard HEAD^
###回退任意版本 
git log
git reset --hard (id)
###撤销修改
####未使用 git add . 之前可以使用 git checkout -- 文件名 对文件进行撤销修改
···git checkout -- text.txt
####使用git add . 之后， 可以通过版本回退撤销修改

