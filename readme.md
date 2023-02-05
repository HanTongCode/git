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
