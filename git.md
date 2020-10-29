##### 学习github的目的：借助github托管项目代码

###### 基本概念：

仓库(Repository)：项目

收藏(Star)：收藏项目，方便下次查看

复制克隆项目(Fork)：克隆项目

发起请求(Pull Request)：代码更新请求

关注(Watch)：关注项目更新，可以接收到通知

事务卡片(Issue)：发现bug，没有成型代码，需要讨论时用

 Github主页：左侧显示用户动态、关注用户、关注仓库的动态，右侧显示所有git库

仓库主页：显示项目信息，如：项目代码，版本，收藏/关注/fork

个人主页：个人信息

##### git工作区域

工作区(Working Directory)：添加、编辑、修改文件等动作

暂存区：暂存已经修改的文件最后统一提交到git仓库

Git Repository(Git仓库)：最终确定的文件保存仓库，成为一个新的版本，对他人可见

git status查看文件状态

工作区提交到暂存区：git add hello.php

暂存区提交到git仓库：git commit -m "提交描述"

##### Git初始化及仓库创建和操作

###### 基本信息设置

1.设置用户名：git config --global user.name 'a597229756a'

2.设置用户名邮箱：git config --global user.name '597229756@qq.com'

###### 初始化一个新的Git仓库

1.创建文件夹（Repository)：mkdir Repository

2.在文件内初始化git（创建git仓库）：git ~/Repository /init，在Repository中生成.git文件，git仓库信息

###### 新增文件/修改文件

1.touch ai.php：新建php文件

2.git status：确认文件状态

3.git add ai.php：提交ai.php文件到暂存区

4.git commit -m "提交描述"：提交ai.php提交到仓库

###### 删除文件

1.rm ai.php：删除文件ai.php

2.git rm ai.php：从git中删除文件

3.git commit -m "提交描述" 

##### Git管理远程仓库

1.将远程仓库（github对应的项目）复制到本地

​	git clone https://github.com/a597229756a/Repository.git

git push ：提交到远程仓库

























