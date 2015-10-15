title: Hello World
date: 2012-10-10 15:01:02
categories: [default]
tags: [markdown, md]
keywords: markdown, md
description: 常用的markdown语法
---



## 七牛图片
![](http://7xnift.com1.z0.glb.clouddn.com/img/2015/openssl.jpg-w400)


<!-- more-->
## Quick Start


### 插入七牛图片

![open ssl](http://7xnift.com1.z0.glb.clouddn.com/img/2015/openssl.jpg)


More info: [Deployment](http://hexo.io/docs/deployment.html)




### 多部署

```
	deploy:
		type: git
		message: update  ##git message建议默认字段update 可以自定义
		repo:
		gitcafe: <repository url>,[branch] ##gitcafe 仓库地址和分支
		github: <repository url>,[branch] ##github 仓库地址和分支

	deploy:
		type: git
		messgae: "update"
		repo:
			github: git@github.com:31526/31526.github.io.git  master
			gitcafe: git@gitcafe.com:31526/31526.git   gitcafe-pages



	deploy:
	type: git
	#messgae: "update"
	repository: git@gitcafe.com:31526/31526.git
	branch: master

	repository: git@github.com:31526/31526.github.io.git
	branch: master





	deploy:
	type: git
	repository: git@gitcafe.com:31526/31526.git
	branch: gitcafe-pages


```

