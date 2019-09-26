Git的说明:
	版本的控制系统都是进行控制文本文件的改动，并不能进行改动二进制文件的改变。所以图片音乐啥的并不能进行控制。
#1初始化一个git仓库。git init.	
#2关于git commit的说明。commit就是相当于一个工作区的快照，也就是工作区下所有文件的快照。当然不可能将整个目录复制一遍。
	主要和上一个版本进行差异对比。将差异进行打包提交记录。
	
#3进行练习分支的版本的倒退:
	创建一个新的分支。git branch dev（这个一般是开发的分支）。
	切换到新创建的分支上去。 git switch dev(branchname)
	然后进行回退版本的即可。 git reset --hard HEAD^(HEAD~回退的次数).
	
#4进行分支的撤销修改的测试:(加上在分支内diff命令的使用 git diff HEAD filename)
	创建一个新的分支。git branch dev2
	切换到新创建的分支上去。 git switch dev(branchname)
	然后进行回退版本的即可。 git reset -- filename 
	当然也可以撤销对stage区域内容 git reset HEAD filename
	
#5进行push到仓库需要注意的是:同名分支进行update。
	push后是进行仓库对仓库相同的update。即使在master中更改了文件push 到没有更新的分支的时候，依然是
	什么东西都是没有更新的。在这里将master分支merger到www分支，然后进行push即可。

#6切换branch的时候需要去commit或者暂存的。否则不会让你进行切换