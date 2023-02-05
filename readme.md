chdir 查看当前路径
git init 初始化 git 仓库
在 Linux 系统中，commit 信息使用单引号包括，windows 系统，commit 信息使用双引号。git commit -m "wrote a readme file"
git status 查看状态
git diff 查看不同
测试
1，查看 git 本地的用户：git config user.name
2，查看 git 本地邮箱：git config user.email
3，修改 git 本地用户： git config --global user.name “用户名”
4，修改 git 本地用户邮箱：git config --global user.email “邮箱地址”

git log 查看日志

git reset
cmd 控制台中换行符默认是 ^ ，而不是\ ，所以它的 more？的意思是问你下一行是否需要再输入，而 ^ 符号就被当做换行符而被 git 命令忽略掉了。解决方法有如下几种：
方法一：加引号：git reset --hard “HEAD^”
方法二：加一个^：git reset --hard HEAD^^
方法三：换成~：git reset --hard HEAD~ 或者 git reset --hard HEAD~1

git add 把文件从工作区>>>>暂存区，git commit 把文件从暂存区>>>>仓库，
git diff 查看工作区和暂存区差异，
git diff --cached 查看暂存区和仓库差异，
git diff HEAD 查看工作区和仓库的差异，
git add 的反向命令 git checkout，撤销工作区修改，即把暂存区最新版本转移到工作区，
git commit 的反向命令 git reset HEAD，就是把仓库最新版本转移到暂存区。
1 暂存区为空使用 git diff：因为此时暂存区为空，此时使用 git diff 同样也是比较工作区和仓库，即和使用 git diff HEAD 结果相同
2 暂存区不为空使用 git diff:因为此时暂存区不为空，此时使用 git diff 比较的就是工作区和暂存区

添加远程 git remote add origin https://github.com/ice-Han666/git.git
第一次提交远程 git push -u origin master

查看远程库 git remote -v
删除 git remote rm origin

查看分支 git branch
创建分支 git branch <name>
创建并切换分支 git checkout -b dev / git switch -c dev
合并分支到当前分支 git merge <name>
删除分支 git branch -d <name>
