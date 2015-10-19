title: git经验小提示
date: 2012-11-12 22:28:10
updated: 2012-11-12 22:28:10
categories: [tools]
tags: [git, github]
keywords: git, github, tools
description: git经验小提示
---


git的一些常用操作




<!--more-->


### Git常用操作

#### 放弃本地修改，强制更新为线上版本

> git fetch --all
> git reset --hard origin/master 


### Git ssh key 生成步骤

参考：<http://git-scm.com/book/zh/ch4-3.html>

#### 设置Git的user name 和 email：
	git config --global user.name "yourname"
    git config --global user.email "youremail"

#### 生成ssh密钥：
	ssh-keygen -t rsa -C "youremail"
连续按三次回车，密码为空
得到两个文件 id_rsa 和 id_rsa.pub, 一般存储在 ~/.ssh/ 目录下
其中id_rsa为私钥，妥善保管不要外泄，id_rsa.pub为公钥

#### 查看刚刚生成的公钥
	cat ~/.ssh/id_rsa.pub




### git提交的时候文件名过长或者文件夹太深导致路径过长
git pull aborted with error filename too long

解决办法：

	git config core.longpaths true

参考：<http://stackoverflow.com/questions/21123415/git-pull-aborted-with-error-filename-too-long>





### 当出现 modified content in submodules 时的解决办法

git 提交出现以下提示：

	$ git status
	On branch develop
	Your branch is up-to-date with 'origin/develop'.
	Changes not staged for commit:
	  (use "git add <file>..." to update what will be committed)
	  (use "git checkout -- <file>..." to discard changes in working directory)
	  (commit or discard the untracked or modified content in submodules)

	        modified:   themes/next (modified content)

解决办法，新建 --.gitmodules--文件

	echo "" >> .gitmodules

在新建的.gitmodules文件内写入：

	[submodule "themes/next"]
		path = themes/next
	    url = git://github.com/iissnan/hexo-theme-next.git
	    ignore = dirty

提示：url为子模块的git地址

参考：http://www.nils-haldenwang.de/frameworks-and-tools/git/how-to-ignore-changes-in-git-submodules


