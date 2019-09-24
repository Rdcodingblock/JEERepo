Git的步骤:
	1.使用cd 进行相关的目录下，然后使用git init进行相关的初始化。这个时候通过ls -a就可以
发现产生了一个.git的目录。一般这个目录不要随便的动。否则容易的损坏repo.
	2.git config --global user.name "Your Name"  设置git 仓库的name
 	   git config --global user.email "email@example.com" 设置git 仓库的email地址。而--global 参数表示对分布式的所有仓库都设置为这两个参数。
当然也可以对单独的repo进行设置。
	3.git进行添加需要提交进行版本控制的文件。可以使用的通配符进行代替所有的文件。使用git add fireName
	4.提交版本控制的文件。git commit -m comment of the fires  -m参数的作用就是为了去给这次的提交加上相关的描述。
	5.Git也是一样，每当你觉得文件修改到一定程度的时候，就可以“保存一个快照”，这个快照在Git中被称为commit。一旦你把文件改乱了，或者误删了文件，还可以从最近的一个commit恢复，
	然后继续工作，而不是把几个月的工作成果全部丢失。也就是Git中的commit也就是一个快照而已。
	6.注意的是:看到的一大串类似1094adb...的是commit id  在git中存在的一大堆的数字是commit的ID 至于设置的原因就是git分布式的原因。
	要随时掌握工作区的状态，使用git status命令。如果git status告诉你有文件被修改过，用git diff可以查看修改内容。
	7.git的版本的回退:使用的就是一个head指针来完成相关的内容。head表示当前的版本的。head^表示进行回退一个版本。head^^表示回退两个版本。
	当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。
	8.Git的版本回退速度非常快，因为Git在内部有个指向当前版本的HEAD指针，当你回退版本的时候，Git仅仅是把HEAD指回去。然后顺便把工作区的文件更新了。使用的方式git reset --hard HEAD^^（HEAD~10）（SHA码）
	9.也可以对回退本身就行回退。回退的方式就是进行git reflog。然后在进行执行git reset --hard SHA码即可。
	10.将本地的仓库的推送给GitHub上的仓库。
		推送存在两种方式。一种是ssh方式。（要事先生成ssh.pub公钥 ）另外一种就是https的方式。
		进行的远程的推送的方式 git push origin master 在第一次的进行push的时候。需要加上-u 参数来进行初始化等等。
	


