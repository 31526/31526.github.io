title: hexo-develop
date: 2015-10-14 11:14:21
tags:
---

hexo备注

<!-- more -->

### Next主题

	https://github.com/iissnan/hexo-theme-next


#### 独立居中的引用

> 带上下分割线的引用，引用内文本将自动居中。适用于单行引用文本的场景。


![](http://iissnan.com/nexus/next/blockquote-center.png)

	<!-- HTML -->
	<blockquote class="blockquote-center">blah blah blah</blockquote>

	<!-- Built-in tag (Require NexT 0.4.5 or above) -->
	{% centerquote %}blah blah blah{% endcenterquote %}

#### 图片将自动扩展 26%，突破文章宽度。

![](http://iissnan.com/nexus/next/full-image.png)

	<!-- HTML -->
	<img src="/image-url" class="full-image" />

	<!-- Built-in tag (Require NexT 0.4.5 or above) -->
	{% fullimage /image-url, alt, title %}




#### 自定义页面内容区域的宽度

> 编辑主题的 __source/css/_variables/custom.styl__ 文件，新增变量：

	$content-desktop = 700px  // 修改成你期望的宽度



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

