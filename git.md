##### 学习github的目的：借助github托管项目代码

###### 团队内部协作

![](G:\Git\gitnote_cz\image\微信截图_20201101083347.png)

###### 团队外部协作

![](G:\Git\gitnote_cz\image\微信截图_20201101083431.png)

###### 基本概念：

​	仓库(Repository)：项目
​	收藏(Star)：收藏项目，方便下次查看
​	复制克隆项目(Fork)：克隆项目
​	发起请求(Pull Request)：代码更新请求
​	关注(Watch)：关注项目更新，可以接收到通知
​	事务卡片(Issue)：发现bug，没有成型代码，需要讨论时用
​	Github主页：左侧显示用户动态、关注用户、关注仓库的动态，右侧显示所有git库
​	仓库主页：显示项目信息，如：项目代码，版本，收藏/关注/fork

##### git工作区域

​	工作区(Working Directory)：写代码的地方
​	暂存区：临时存储
​	Git Repository(Git仓库)：存储每一个历史版本
​	创建文件夹（Repository)：mkdir Repository
​	在文件内初始化git（创建git仓库）：git ~/Repository /init，在Repository中生成.git文件，git仓库信息
​	git status查看文件状态
​	工作区提交到暂存区：git add hello.php
​	暂存区恢复到工作区：git rm --cache hello.php
​	暂存区提交到git仓库：git commit -m "提交描述" hello.php

##### 查看历史版本：

git log 		git log --pretty=oneline		git log --oneline		git reflog
	回到9bea226 这个版本：git reset --hard 9bea226 	
	只能后退,后退1个版本：git reset --hard HEAD^		git reset --hard HEAD ~1
		reset  --soft：仅仅在本地哭移动head  
				   --mixed： 在本地库移动head，重置暂存区	
  	             --head：本地库移动head，重置暂存区和工作区 
工作区修改文件和暂存区比较：git diff hello.php
工作区和仓库上一个版本进行比较：git diff HEAD^ hello.php

##### Git初始化及仓库创建和操作

###### 	设置签名

​	签名的作用：是用来区分开发人员的标志，邮箱有没有都行
​	项目即便签名：仅当前本地库范围内有效，保存文件位置./.git/config
​		1.设置用户名：git config user.name 'a597229756a'
​		2.设置用户名邮箱：git config  user.email '597229756@qq.com'
​	系统级别签名：操作系统的用户范围，文件保存位置~/.gitconfig
​		1.设置用户名：git config --global user.name 'a597229756a'
​		2.设置用户名邮箱：git config --global user.email '597229756@qq.com'

###### 	分支管理

![image-20201031005303775](C:\Users\ADMIN\AppData\Roaming\Typora\typora-user-images\image-20201031005303775.png)

​		创建分支：git branch [分之名]
​		查看分支：git branch -v
​		切换分支：git checkout[分支名]
​		合并分支：1.切换到被合并分之上。2.执行merge命令，git merge [分支名]。
​		冲突解决：1.修改冲突文件。2.git add [文件名]。3.git commit -m “描述”。

##### Git分支管理机制

###### 	分支的创建

![image-20201101094053373](G:\Git\gitnote_cz\image\image-20201101094053373.png)

##### Git文件管理原理

###### 	git的提交对象

![](G:\Git\gitnote_cz\image\微信截图_20201101093357.png)

###### 	提交对象及父对象形成的链条

![image-20201101093820769](G:\Git\gitnote_cz\image\image-20201101093820769.png)

##### Git管理远程仓库

​	在本地创建远程库地址别名
​		查看别名：git remote -v 
​		起别名：git remote add gitnote_cz  https://github.com/a597229756a/gitnote_cz.git
​		推送：git push gitnote_cz master
​				

​	将远程仓库（github对应的项目）复制到本地
​		git clone https://github.com/a597229756a/gitnote_cz.git
​		git push ：提交到远程仓库

##### 解决git push错误

​	the requested URL returned error: 403 Forbidden while accessing
​	答案：似有项目，没有权限，输入用户名密码，或者远程地址采用这种类型：vi .git/config
​	[remote "origin"]
​		url = https://github.com/用户名/仓库名.git
​	[remote "origin"]
​		url = https://用户名:密码@github.com/用户名/仓库名.git

##### Github Pages搭建网站

###### 搭建步骤

​	1.创建个人站点->创建仓库（仓库名必须是“用户名.github.io”)
​	2.在仓库下新建index.html
​	3.访问https://a597229756a.github.io/index.html

##### Project Pages项目站点

​	https://a597229756a.gitthub.io/仓库名

###### 搭建步骤

​	1.进入项目主页，点击settings
​	2.在settings页面，点击lanuch automatic page generator(自动生成主题页面)
​	3.新建站点基础信息设置，选择主题，生成网页















