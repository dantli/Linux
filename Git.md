+ 删除文件
	+  从版本库中删除：`git remove <file>`，删除后要`git commit`
	+  误删恢复：从版本库恢复，`git checkout  --<file>`
+ 关联本地仓库和远程仓库
	+  `git remote add origin git@github.com:<account>/<project>.git`，origin是远程库的名字，这是Git默认的叫法，也可以改成别的，但是origin这个名字一看就知道是远程库。
	+ 把本地推送到远程仓库，`git push -u origin master`，第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令，`git push` 。
+ git主分支为master，master指向提交，HEAD指向当前分支
+ 分支处理：
	+ 创建分支：`git branch <branchName>`
	+ 切换分支：`git check out <branchName>`
	+ 创建并切换分支：`git checkout -b <branchName>`，`-b`表示创建并切换
	+ 查看分支： `git branch -<parameter>`, `-a`查看远程和本地分支，`-v`查看远程分支
	+ 删除分支： `git branch -d branchName`删除分支
	+ 合并分支：`git merge <branchName>`，合并指定分支到当前分支。
+ 分支管理策略：
	+  master分支应该是非常稳定的，也就是仅用来发布新版本，平时不能在上面开发
	+  开发都在dev分支上，也就是说，dev分支是不稳定的，到某个时候，比如1.0版本发布时，再把dev分支合并到master上，在master分支发布1.0版本
	+  每个人都基于dev分支上开发，每个人都有自己的分支，时不时地往dev分支上合并就可以了
	+  有了bug就需要修复，每个bug都可以通过一个新的临时分支来修复，修复后，合并分支，然后将临时分支删除。
	+  通常，合并分支时，如果可能，Git会用Fast forward模式，但这种模式下，删除分支后，会丢掉分支信息。如果要强制禁用Fast forward模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信息。
	+ 禁用Fast forward模式: `git merge --no-ff -m "Commit descirbe message" <branchName>`
+ 暂存工作区：
	+  当想转到其他分支上进行一些工作。你又不想提交进行了一半的工作时，可以“储藏”目录的中间状态，随时可以重新应用。
	+  暂存：`git stash`
	+ 查看现有储藏：`git stash list`
	+  重新应用暂存：`git stash apply --index`
+ 查看远程库信息：`git remote -v`
