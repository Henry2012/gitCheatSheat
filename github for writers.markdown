#Let github.com work for me 
1. Putty Key Generator
	* Generate
	* Save public **AND** private keys to the directory (C:\Users\QQ.Han\.ssh)
		* private key: *.ppk
		* there are 2 formats for saving a public key.  
2. Copy public key to https://github.com/settings/ssh
3. git clone - TortoiseGit
	* Load Putty Key: *.ppk
	* URL: git@github.com:Henry2012/gitCheatSheat.git
4. .gitignore
	* 父文件夹有了这个文件后，子文件夹就不需要了
	* 如果父文件夹里有io/,则忽略父文件夹里所有以io命名的子文件夹，或者子子文件夹
5. 使用git多终端办公步骤：
	1. Bitbucket(Github)创建新的Repo
	2. ~~为这个库配置Deployment Key（利用PuttyGen本地生成）~~
	3. [为整个Bitbucket账号设置SSH Keys](https://bitbucket.org/account/user/QiqunH/ssh-keys/)
	3. 在Eclipse里同步这个库，利用egit管理
		* 直接import projects from git
		* pydev project需要注意保证： .project和.pydevproject里的project名称和项目名称保持一致，不然eclipse import projects时会出现错误  
		* egit管理的一个好处是可以直观地看出哪些库有了更新
4. 需要在tortoisegit中设置用户名及邮箱
5. SSH2 (eclipse) --> Load Existing Key 需要load没有后缀的文件（这里通过eclipse -> SSH2 -> Key Management -> Gernerate RSA Key生成了两个文件，一个没有后缀，一个是以pub结尾）
6. PuttyGen load private key,需要load ppk格式的文件，生成一个public key
7. [bitbucket](https://bitbucket.org/account/user/QiqunH/ssh-keys/ "bitbucket")的SSH keys和deployment keys不一样
#Attention
1. 3个不同的key文件
	* id_rsa.ppk <-- putty private key,也就是，ppk是利用puttygen生成的私钥，是Tortoise Git需要的格式
	* id_rsa <-- 没有后缀名的私钥，foreign key (OpenSSH SSH-2 private key),是egit需要的格式
	* id_rsa.pub <-- 公钥
2. public key和github SSH之间的交互

#Q & A
1. 右键不显示git clone
	* 安装tortoisegit
2. SSH文件更改之后如何关联
	* TortoiseGit --> Git -> Remote -> origin -> Putty
3. **Bitbucket需要为每一个repo设置SSH Key，如何避免这么麻烦的操作？**
4. **利用egit如何实现多个projects同时commit & push?**
	* 杰哥：git repo是一个操作单位，不可以跨repo同时commit or push 	
5. 为什么egit只可以commit，不可以push；而对应的文件夹里却能实现commit & push?

