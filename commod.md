# Linux命令

+ 命令行快捷键
    +  光标回到命令行首：`Ctrl+a` （a：ahead） 
    +  光标回到命令行尾: `Ctrl+e` （e：end）
    +  删除光标处到行尾的字符: `Ctrl+k`  （剪切）
    +  删除光标处到行首的字符：`Ctrl+u` （剪切）
    +  删除光标左面的单词: `Ctrl+w`
    +  删除光标右面位置的单词：`Esc+d`
    +  粘贴剪切内容：`Ctrl+y`
    +  清屏操作: `Ctrl+l`
    +  在单词之间跳转: `ctrl+左右键`
    +  往回(左)移动一个字符: `Ctrl+f` 
    +  往回(右)移动一个字符：`Ctrl+b`
    +  往回(左)移动一个单词: `Alt+f` 
    +  往回(右)移动一个单词：`Alt+b`
    +  搜索历史命令: `Ctrl+r`
    +  从历史搜索模式（Ctrl – r）退出: `Ctrl+g`
    +  移动到当前单词的开头: `Esc+b`
    +  移动到当前单词的结尾: `Esc+f` 
    +  上一个命令的后面的参数: `Esc+.`
    +  颠倒光标所在处及其相邻单词的位置 :`Esc+t`
+ Linux下复制粘贴快捷键
    +  复制命令：Ctrl + Insert  组合键　　或　　用鼠标选中即是复制     或    Ctrl + Shift + C  组合键.
    +  粘贴命令：Shift + Insert  组合键　 或　　单击鼠标滚轮即为粘贴   或    Ctrl + Shift + V  组合键.
+  wc统计
    +  -c或--bytes或——chars：只显示Bytes数；
    +  -l或——lines：只显示列数；
    +  -w或——words：只显示字数。
+ 输出：除了echo,还有printf
    +  c语言的格式，%s %c %d %f都是格式替代符，-表示左对齐，没有则表示右对齐
+ 输入输出重定向：stdin的文件描述符为0，stdout 的文件描述符为1，stderr的文件描述符为2
`
    +  command > file 	将输出重定向到 file。
    +  command < file 	将输入重定向到 file。
    +  command >> file 	将输出以追加的方式重定向到 file。
    +  n > file 	将文件描述符为 n 的文件重定向到 file。
    +  n >> file 	将文件描述符为 n 的文件以追加的方式重定向到 file。
    +  n >& m 	将输出文件 m 和 n 合并。
    +  n <& m 	将输入文件 m 和 n 合并。
`
+ 打包压缩:
    +  bzip2 file1 压缩一个叫做 'file1' 的文件 
    +  gunzip file1.gz 解压一个叫做 'file1.gz'的文件 
    +  gzip file1 压缩一个叫做 'file1'的文件 
    +  gzip -9 file1 最大程度压缩 
    +  rar a file1.rar file1 file2 dir1 同时压缩 'file1', 'file2' 以及目录 'dir1' 
    +  rar x file1.rar 解压rar包 
    +  unrar x file1.rar 解压rar包 
    +  tar -cvf archive.tar file1 file2 dir1 创建一个包含了 'file1', 'file2' 以及 'dir1'的档案文件 
    +  tar -tf archive.tar 显示一个包中的内容 
    +  tar -xvf archive.tar 释放一个包 
    +  tar -cvfj archive.tar.bz2 dir1 创建一个bzip2格式的压缩包 
    +  tar -xvfj archive.tar.bz2 解压一个bzip2格式的压缩包 
    +  tar -cvfz archive.tar.gz dir1 创建一个gzip格式的压缩包 
    +  tar -xvfz archive.tar.gz 解压一个gzip格式的压缩包 
    +  zip -r file1.zip file1 file2 dir1 将几个文件和目录同时压缩成一个zip格式的压缩包 
    +  unzip file1.zip 解压一个zip格式压缩包 
+ 文件搜索
    +  find / -name file1 从 '/' 开始进入根文件系统搜索文件和目录 
    +  find / -user user1 搜索属于用户 'user1' 的文件和目录 
    +  find /home/user1 -name \*.bin 在目录 '/ home/user1' 中搜索带有'.bin' 结尾的文件 
    +  find /usr/bin -type f -mtime -10 搜索在10天内被创建或者修改过的文件 
    +  locate \*.ps 寻找以 '.ps' 结尾的文件 - 先运行 'updatedb' 命令 
    +  whereis 
+ grep 
    +  grep [options] PATTERN [FILE...],PATTERN支持正则表达式，options如下：
    +  -c:只输出匹配行的计数
    +  -I:不区分大小写(只适用于单字符)。
    +  -h:查询多文件时不显示文件名。
    +  -l:查询多文件时只输出包含匹配字符的文件名
    +  -n:显示匹配行及行号。
    +  -s:不显示不存在或无匹配文本的错误信息。
    +  -v:显示不包含匹配文本的所有行。
    +  -R: 连同子目录中所有文件一起查找 
+ 查看文件内容 
    +  cat file1 从第一个字节开始正向查看文件的内容 
    +  tac file1 从最后一行开始反向查看一个文件的内容 
    +  more file1 查看一个长文件的内容 
    +  less file1 类似于 'more' 命令，但是它允许在文件中和正向操作一样的反向操作 
    +  head -2 file1 查看一个文件的前两行 
    +  tail -2 file1 查看一个文件的最后两行 
    +  tail -f /var/log/messages 实时查看被添加到一个文件中的内容 
+ 创建链接：：ln [option] source_file dist_file   （source_file是待建立链接文件的文件，dist_file是新创建的链接文件）
+ 作业管理
    + 后台执行的&
        如想将/etc 备份为/tmp/ect.tar.gz时不想等待，可以这样做：
        tar -zpcf  /tmp/etc.tar.gz /etc &
    +  将当前作业放到后台暂停[ctrl] -z 
 
    +  观察当前后台作业状态：jobs 
        jobs [-lrs]
        -l 除了列出作业号之外，同时列出PID
        -r 仅列出正在后台运行的作业
        -s 仅列出正在后台暂停的作业
    +  将后台作业拿到前台处理：fg 
+ 进程管理
    +  ps 
            ps -l :将当前属于自己登陆的PID与相关信息展示，参数说明见下图：
            ps aux ：列出当前所有正在内存中的进程
            ps -lA : 显示出所有的进程
            ps -axjf 列出类似进程树的进程显示
    +  top [-d]  [-bnp]
            每2s更新一次：top -d 2
            只观察一个进程 top -d 2 -p10660 
        结果参数说明：
        PR：priority的简写，进程的优先执行顺序，越小越早执行
        NI:nice的简写，，与priority有关，也是越小越早执行
        TIME+：CPU的使用时间累加
 
+ 进程删除
        kill -9  PID

+ ifconfig
    +  查看网卡信息：`ifconfig`
    +  关闭网卡eth0：`sudo ifconfig eth0 down`
    +  开启网卡eth0：`sudo ifconfig eth0 up`
    +  给eth0配置临时IP：`sudo ifconfig eth0 IP`
+ netstat
    +  netstat [选项] 显示网络连接、路由表和网络接口信息
    +  -a 显示所有socket,包括正在监听的。
    +  -c 每隔1秒就重新显示一遍,直到用户中断它。
    +  -i 显示所有网络接口的信息,格式同“ifconfig -e”。
    +  -n 以网络IP地址代替名称,显示出网络连接情形。
    +  -r 显示核心路由表,格式同“route -e”。
    +  -t 显示TCP协议的连接情况。
    +  -u 显示UDP协议的连接情况。
    +  -v 显示正在进行的工作 

+ HTTP压测工具wrk:

```
使用方法: wrk <选项> <被测HTTP服务的URL>                            
  Options:                                            
    -c, --connections <N>  跟服务器建立并保持的TCP连接数量  
    -d, --duration    <T>  压测时间           
    -t, --threads     <N>  使用多少个线程进行压测   
                                                      
    -s, --script      <S>  指定Lua脚本路径       
    -H, --header      <H>  为每一个HTTP请求添加HTTP头      
        --latency          在压测结束后，打印延迟统计信息   
        --timeout     <T>  超时时间     
    -v, --version          打印正在使用的wrk的详细版本信息
                                                      
  <N>代表数字参数，支持国际单位 (1k, 1M, 1G)
  <T>代表时间参数，支持时间单位 (2s, 2m, 2h)

```

# Git学习

+ 把目录变成Git可以管理的仓库:`git init`
+ 把文件添加到仓库:`git add <file>`
+ 把文件提交到仓库：`git commit -m "<message>" message为本次提交的说明,清楚有意义，第一个首字母大写`
+ 修正未merge的commit: `git commit --amend`,然后`git push -f` 
+ 查看仓库当前的状态：`git status`
+ 查看看具体修改了什么内容:`git diff <file>`
+ 提交历史记录：`git log`
+ 版本回退：`git reset --hard commit_id`。 commit_id可以使用`git log`查看，也可以使用HEAD表示，HEAD表示当前版本，HEAD^2表示上上一版本，可缩写为HEAD^num表示回退的版本
+ 命令历史记录：`git reflog`
+ 撤销修改:`git checkout -- <file>`,命令中的--很重要，没有--，就变成了“切换到另一个分支”的命令
    +  修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
    +  添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
    +  `git reset HEAD <file>`也可以把暂存区的修改撤销掉
+ 删除文件：
    +  删除本地：`rm <file>`
    +  删除版本库：`git rm <file>` 然后 `git commit`
    +  误删除，恢复到最新版：`git checkout --<file>`
+ 本地仓库与远程仓库关联：`git remote add origin git@server-name:path/project-name.git`
+ 本地库内容推送到远程库上:`git push origin master`
+ 克隆一个本地库：`git clone git@server-name:path/project-name.git`
+ git实现fork的项目与原项目同步:利用本地仓库作为中转，为本地的项目添加两个远程信息，拉取原仓库的新代码，push到自己的仓库上，就达到了“同步”
    +  同步fork项目和本地仓库
    +  查看项目的远程分支：`git remote -v`
    +  为项目添加原项目远程分支：`git remote add <upstream> <branchAddress>`.其中upstream是远程分支名，branchAddress是原项目仓库。
    +  从upstream分支拉取得，同步本地仓库和原项目仓库：`git pull upstream master`
    +  将本地仓库提交到自己主页分支：`git push origin master`
+ 拉取未merge的patch到本地进行测试：
    +  配置`~/.gitconfig`,添加:`  mr = !sh -c 'git fetch $1 merge-requests/$2/head:mr-$1-$2 && git checkout mr-$1-$2' -`
    +  拉取：`git mr upstream <mrId>`
+ git主分支为master，master指向提交，HEAD指向当前分支
+ 分支处理
    + 创建分支：`git branch <branchName>`
    + 切换分支：`git check out <branchName>`
    + 创建并切换分支：`git checkout -b <branchName>`，`-b`表示创建并切换
    + 查看分支： `git branch -<parameter>`, `-a`查看远程和本地分支，`-v`查看远程分支
    + 删除分支： `git branch -d branchName`删除分支
    + 合并分支：`git merge <branchName>`，合并指定分支到当前分支
+ 分支管理策略：
    +  master分支应该是非常稳定的，也就是仅用来发布新版本，平时不能在上面开发  
    +  开发都在dev分支上，也就是说，dev分支是不稳定的，到某个时候，比如1.0版本发布时，再把dev分支合并到master上，在master分支发布1.0版本
    +  每个人都基于dev分支上开发，每个人都有自己的分支，时不时地往dev分支上合并就可以了
    +  有了bug就需要修复，每个bug都可以通过一个新的临时分支来修复，修复后，合并分支，然后将临时分支删除。
    +  通常，合并分支时，如果可能，Git会用Fast forward模式，但这种模式下，删除分支后，会丢掉分支信息。如果要强制禁用Fast forward模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信
息。
    + 禁用Fast forward模式: `git merge --no-ff -m "Commit descirbe message" <branchName>`
+ 暂存工作区：
    +  当想转到其他分支上进行一些工作。你又不想提交进行了一半的工作时，可以“储藏”目录的中间状态，随时可以重新应用。
    +  暂存：`git stash`
    + 查看现有储藏：`git stash list`
    +  重新应用暂存：`git stash apply --index`
+ 查看远程库信息：`git remote -v`


# Docker学习

## 免sudo使用docker命令

+  因为使用的是`sudo`安装`docker`，所以会导致以普通用户登录的状况下，在使用docker images时必须添加sudo.否则出现错误：

```
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock
```
问题原因是`/var/run/docker.sock`权限问题。
    +  修改权限sudo chmod a+rw /var/run/docker.sock
    +  如果还没有 docker group 就添加一个:`sudo groupadd docker`
    +  将用户加入该 group 内:`sudo gpasswd -a ${USER} docker`
    +  重启 docker 服务:`sudo docker service restart`
    +  切换当前会话到新 group 或者重启 X 会话:`newgrp - docker`
## 常用命令
+ 查找镜像：`docker search <name>`
+ 拉取镜像：`docker pull <name>:tag` 如：

```
docker pull ubuntu:latest
docker pull registry.hub.docker.com/ubuntu:latest
```
+ 查看本地镜像仓库：`docker images`
+ 启动镜像：`docker run -it <images>` 
    +  -it 表示运行在交互模式，是-i -t的缩写，即-it是两个参数：-i和-t。前者表示打开并保持stdout，后者表示分配一个终端（pseudo-tty）一般这个模式就是可以启动bash，然后和容器有命令行的交互
+ 退出容器
    +  退出容器不关闭:`Ctrl+P+Q`
    +  退出关闭：`exit`
    +  exit后会关闭容器，使用下面流程恢复：
    ```
    启动/停止/重启容器：docker stop/start/restart <name>
    进入容器：docker attach <>
    删除容器或镜像：`docker rm container_id/image_id`，删除镜像前必须先删除以此镜像为基础的容器（哪怕是已经停止的容器）

    ```
