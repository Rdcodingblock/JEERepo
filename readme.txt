Git的步骤:
	1.使用cd 进行相关的目录下，然后使用git init 进行相关的初始化。这个时候通过ls -a就可以
发现产生了一个.git的目录。一般这个目录不要随便的动。否则容易的损坏repo.
	2.git config --global user.name "Your Name"  设置git 仓库的name
 	   git config --global user.email "email@example.com" 设置git 仓库的email地址。而--global 参数表示对分布式的所有仓库都设置为这两个参数。
当然也可以对单独的repo进行设置。
	

