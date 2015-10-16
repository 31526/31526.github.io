# README.md


## Hexo

### Hexo Plugins



## Next

### Next Setting

#### 自定义页面内容区域的宽度

编辑主题的 themes/next/source/css/_variables/custom.styl 文件，新增变量：

> $content-desktop = 820px  // 修改成你期望的宽度



#### .gitmodules 文件

```
[submodule "themes/next"]
	path = themes/next
    url = git://github.com/iissnan/hexo-theme-next.git
    ignore = dirty
```



#### themes/next 下的 .gitignore 文件备份

> themes/next/.gitignore

```
.DS_Store
.idea/
*.log
node_modules/

# Ignore unused verdors' files
source/vendors/fancybox/*
!source/vendors/fancybox/source/
```


## GitHub

### Github


## QiNiu七牛

> https://github.com/gyk001/hexo-qiniu-sync




### Coding备份Hexo博客代码和Next主题代码

> 为避免github不稳定和方便在多台机器上写作，特在Coding备份Hexo博客代码和Next主题代码
> git@git.coding.net:31526/31526.github.io.git

#### 已有项目
git remote add origin git@git.coding.net:31526/31526.github.io.git
git push -u origin master



#### 现有项目
mkdir 31526.github.io
cd 31526.github.io
git init
echo "# 31526.github.io" >> README.md
git add README.md
git commit -m "first commit"
git remote add origin git@git.coding.net:31526/31526.github.io.git
git push -u origin master
