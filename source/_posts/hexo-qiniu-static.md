title: Hexo 使用七牛云做图床并存储静态资源
date: 2014-02-12 22:28:10
updated: 2014-02-12 22:28:10
categories: [tools]
tags: [hexo, 七牛, git, github]
keywords: hexo, git, github, tools
description:  Hexo 使用七牛云做图床并存储静态资源
---


Hexo 使用七牛云做图床并存储静态资源

<!-- more-->



### 七牛云存储插件

> https://github.com/gyk001/hexo-qiniu-sync


#### 同步上传命令行

> hexo qiniu i # 功能：显示插件版本，作者及Github地址信息等
> hexo qiniu s # 功能：同步静态资源到七牛空间
> hexo qiniu s2 # 功能：同步静态资源到七牛空间，且会同步上传那些本地与七牛空间有差异的文件。


#### 配置


```
#七牛云存储设置
##域名 7xnift.com1.z0.glb.clouddn.com
##offline       是否离线. 离线状态将使用本地地址渲染
##sync          是否同步
##bucket        空间名称.
##access_key    上传密钥AccessKey
##secret_key    上传密钥SecretKey
##dirPrefix     上传的资源子目录前缀.如设置，需与urlPrefix同步
##urlPrefix     外链前缀.
##local_dir     本地目录.
##update_exist  是否更新已经上传过的文件(仅文件大小不同或在上次上传后进行更新的才会重新上传)
##image/js/css  子参数folder为不同静态资源种类的目录名称，一般不需要改动
##image.extend  这是个特殊参数，用于生成缩略图或加水印等操作。具体请参考http://developer.qiniu.com/docs/v6/api/reference/fop/img/
##              可使用基本图片处理、高级图片处理、图片水印处理这3个接口。例如 ?imageView2/2/w/500 即生成宽度最多500px的缩略图
qiniu:
  offline: false
  sync: true
  bucket: github
  access_key: access_key
  secret_key: secret_key
  dirPrefix:
  urlPrefix: http://7xnift.com1.z0.glb.clouddn.com
  local_dir: static
  update_exist: true
  img:
    folder: img
    extend:
  js:
    folder: js
  css:
    folder: css
  up:
  	folder: upload

```


#### 在页面中使用

```
	{% qnimg imageFile attr1:value1 attr2:value2 'attr3:value31 value32 value3n' [extend:?imageView2/2/w/600 | normal:yes] %}
	{% qnjs jsFile attr1:value1 attr2:value2 'attr3:value31 value32 value3n' %}
	{% qncss cssFile attr1:value1 attr2:value2 'attr3:value31 value32 value3n' %}
```

![](http://7xnift.com1.z0.glb.clouddn.com/img/2015/london-bridge.jpg-w320)


#### 图片测试

> {% qnimg 2015/london-bridge.jpg-w200 %}

{% qnimg 2015/london-bridge.jpg-w320  alt:alt图片说明 title:titlelondon %}



#### show photo 

![Title说明](http://7xnift.com1.z0.glb.clouddn.com/img/2015/london-bridge.jpg-w200 "Alt说明")



> http://7xnift.com1.z0.glb.clouddn.com/img/2015/london-bridge.jpg



{% qnimg 2015/london-bridge.jpg-w200 %}







### Markdown语法



#### 区块引用

demo:

> This is a blockquote

code:

  > This is a blockquote



#### 强调

This is a list item with two _paragraphs._ Lorem ipsum dolor
    sit amet, __consectetuer__ adipiscing elit. *Aliquam* hendrerit
    mi **posuere lectus**.

下面换行

-------------------------------

#### 链接内容定义的形式为：
```
方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
接着一个冒号
接着一个以上的空格或制表符
接着链接的网址
选择性地接着 title 内容，可以用单引号、双引号或是括弧包着
下面这三种链接的定义都是相同：

[id]: <http://example.com/>  "Optional Title Here"

```


#### 真实的地球形状是这样的

![](http://7xnift.com1.z0.glb.clouddn.com/img/2015/earth-round.gif)


#### 图片链接

  <code>
    > [![](http://7xnift.com1.z0.glb.clouddn.com/img/2015/duola-a-dream.jpg-w200 "duolaDream")](http://7xnift.com1.z0.glb.clouddn.com/img/2015/duola-a-dream.jpg)
  <code>

photo

![](http://7xnift.com1.z0.glb.clouddn.com/img/2015/duola-a-dream.jpg-w200)

change

[![多啦A梦](http://7xnift.com1.z0.glb.clouddn.com/img/2015/duola-a-dream.jpg-w200)](http://7xnift.com1.z0.glb.clouddn.com/img/2015/duola-a-dream.jpg-w400)




[![BeijingCBD](http://7xnift.com1.z0.glb.clouddn.com/img/2015/beijing-cbd.jpg "北京CBD夜景")](http://7xnift.com1.z0.glb.clouddn.com/img/2015/beijing-cbd.jpg)




![多啦A梦](http://7xnift.com1.z0.glb.clouddn.com/img/2015/duola-a-dream.jpg-w280)

![OpenSSL Team](http://7xnift.com1.z0.glb.clouddn.com/img/2015/openssl.jpg-w320)

