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