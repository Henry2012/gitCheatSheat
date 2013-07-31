#Let github.com work for me 

1. Putty Key Generator
	* Generate
	* Save public **AND** private keys to the directory (C:\Users\QQ.Han\.ssh)
		* private key: *.ppk
2. Copy public key to https://github.com/settings/ssh
3. git clone - TortoiseGit
	* Load Putty Key: *.ppk
	* URL: git@github.com:Henry2012/gitCheatSheat.git
4. .gitignore
	* 父文件夹有了这个文件后，子文件夹就不需要了
	* 如果父文件夹里有io/,则忽略父文件夹里所有以io命名的子文件夹，或者子子文件夹
5. 使用git多终端办公步骤：
	1. Bitbucket(Github)创建新的Repo
	2. 为这个库配置Deployment Key，利用PuttyGen本地生成
	3. 在Eclipse里同步这个库，利用egit管理
		* 直接import projects from git
		* pydev project需要注意保重： .project和.pydevproject里的project名称和项目名称保持一致，不然eclipse import projects时会出现错误  
4. 需要在tortoisegit中设置用户名及邮箱
	
#Attention
1. 理解ppk (private key)的来由
2. public key和github SSH之间的交互

#Q & A
1. 右键不显示git clone
	* 安装tortoisegit
2. SSH文件更改之后如何关联
	* TortoiseGit --> Git -> Remote -> origin -> Putty
3. **Bitbucket需要为每一个repo设置SSH Key，如何避免这么麻烦的操作？**
