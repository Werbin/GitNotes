### 本篇笔记总结自[git官网](https://git-scm.com/)、[廖雪峰Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)、[Learn Git in 20 Minutes](https://www.youtube.com/watch?v=Y9XZQO1n_7c)
```
git status

git add readme.txt

git commit(先按i调出插入，输入提交信息，esc结束，:wq退出)

git --version

git config user.email "zhenghaochuan9421@gmail.com"

git config user.name "HaoChuan9421"

git config --global user.email "zhenghaochuan9421@gmail.com"(全局配置)

git init

git commit -m "说明文字"

git commit -a -m "说明文字"(自动添加，修改原本存在的文件不需要先git add)

git log

git log --pretty=oneline(单行显示)

git log --graph(图形化显示)

git log --abbrev-commit(commit缩写为七位)

git log --graph --pretty=oneline --abbrev-commit(合并上述)

git add .(添加全部)

git add "*.txt"(通配符，选择所有txt格式文件，包括文件夹里面的)

git rm --cached index.txt(添加index.txt到stage之后将它移除)

git checkout -- index.txt(修改了index.txt，但未add，未commit，将它恢复到上一次add或者commit的状态)

git reset HEAD index.txt(unstage操作，回到最后一次提交的版本)

rm index.txt(删除index.txt，可以使用checkout恢复，这种删除等同于直接从硬盘删除)

git rm index.txt(删除不可恢复，只可以提交)

touch .gitignore (添加忽略文件)

cat index.txt(查看index.txt文件的具体内容)

git branch MyBranch (创建分支)

git checkout MyBranch (切换分支)

git checkout -b MyBranch (创建并切换分支，相当于合并上面两步)

git checkout master (切换到主分支)

git merge MyBranch (合并分支)

git branch -d MyBranch(删除分支)

git add . (先添加)

git stash (隐藏)

git stash apply (显现)

git remote add origin https://git.coding.net/fmw/Miaopiao.git

git push -u origin master

git pull origin master

git reset --hard HEAD^(回退到上个版本)

git reset --hard HEAD^^(回退到上上个版本)

git reset --hard a0c85da(指针指向该版本号的版本)

git reflog(查看所有版本操作记录)

git diff(查看修改)

git diff HEAD -- index.txt(查看指定文件index.txt的修改)

$ ssh-keygen -t rsa -C "youremail@example.com"(生成ssh，一路回车，使用默认值即可，无需设置密码，再把pub添加到GitHub)

git clone git@github.com:HaoChuan9421/GitNotes.git(克隆远端仓库)
```
学习版本冲突
