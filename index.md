### 本篇笔记总结自[git官网](https://git-scm.com/)、[Learn Git in 20 Minutes](https://www.youtube.com/watch?v=Y9XZQO1n_7c)、[廖雪峰Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)。只是简单的起步笔记，满足日常的工作而已。
```
git init

git status

git add readme.txt

git commit(先按i调出插入，输入说明文字，esc结束，:wq退出)

git --version

git config user.email/user.name (查看用户名/邮箱)

git config user.email "zhenghaochuan9421@gmail.com"(设置修改邮箱)

git config user.name "HaoChuan9421"(设置修改用户名)

git config --global user.email "zhenghaochuan9421@gmail.com"(全局配置)

git commit -m "说明文字"

git commit -a -m "说明文字"(自动添加，修改原本存在的文件不需要先git add)

git log

git log --pretty=oneline(单行显示)

git log --graph(图形化显示)

git log --abbrev-commit(commit缩写为七位)

git log --graph --pretty=oneline --abbrev-commit(合并上述)

git add .(添加全部)

git add "*.txt"(通配符，选择所有txt格式文件，包括文件夹内的)

git rm --cached index.txt(添加index.txt到stage之后将它移除)

git checkout -- index.txt(修改了index.txt，但未add，未commit，将它恢复到上一次add或者commit的状态)

git reset HEAD index.txt(unstage操作，回到最后一次提交的版本)

rm index.txt(删除index.txt，可以使用checkout恢复，这种删除等同于直接从硬盘删除)

git rm index.txt(删除不可恢复，只可以提交删除操作)

touch .gitignore (生成忽略文件)

cat index.txt(查看index.txt文件的具体内容)

git branch MyBranch (创建分支)

git checkout MyBranch (切换分支)

git checkout -b MyBranch (创建并切换分支，相当于合并上面两步)

git checkout master (切换到主分支)

git merge MyBranch (当前分支合并MyBranch分支)

git branch -d MyBranch(删除分支)

git branch -D MyBranch(删除未合并的分支时系统会提示不让删除，该命令强行删除)

git add . (先添加)

git stash (隐藏add的内容)

git stash list(查看藏匿区)

git stash apply (显现但是不删除藏匿区)

git stash drop (删除藏匿区,藏匿区的文件也会删除)

git stash pop(显示同时删除藏匿区)

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

vi index.md(在git bash中编辑文件)

git merge --no-ff -m '提示信息' MyBranch (采用非Fast forward模式合并，合并后可以看出曾经做过合并)

git创建分支时，会以当前所在分支为模版创建

git remote -v (查看远端仓库信息，如果没有push权限会只显示fetch)

git push origin dev(push到远端仓库dev分支)

git checkout -b dev origin/dev (git clone下来的只有master分支，如果需要其他分支，如dev分支则需要执行这个命令)

git branch --set-upstream dev origin/dev (设置本地分支与远端分支的链接，否则无法pull)

git branch --set-upstream-to=origin/test(远端有分支，本地没分支时，先在本地创建，然后关联到远端)

git pull (拉取远端最新的代码)

git push origin --delete test(删除远端test分支)

git push origin :test(删除远端test分支)

git tag(查看标签)

git tag v1.0(打标签，默认打在最新一次的commit上)

git tag v0.9 fec145a(给指定的commit打标签，需要commit的版本号，可先使用git log --pretty=oneline --abbrev-commit查看)

git show v1.0(查看标签)

git tag -a v1.1 -m "version 1.1 released" 3628164(打带说明文字的标签，用-a指定标签名，-m指定说明文字)

git tag -d v1.0(删除指定标签，删除标签的操作只是本地操作，不会推送到远程)

git push origin v1.0(推送某个标签到远程)

git push origin --tags(一次性推送全部尚未推送到远程的本地标签)

git push origin :refs/tags/v0.9(删除远程的标签，需要先删除本地的标签git tag -d v0.9，再执行这一步)
```
