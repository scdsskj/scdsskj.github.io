# Hugo模块

探索你最深处的秘密
&lt;!--more--&gt;# Hugo 模块搭建Blog
{{&lt; admonition tip &gt;}}
以这种方式，无需要在 hugo.toml 中配置 theme = &#34;FixIt&#34;。
{{&lt; /admonition &gt;}}

1.将 Hugo 模块 用于主题的最简单方法是将其导入配置中。请参阅 使用 Hugo 模块。

2.初始化 Hugo 模块系统：hugo mod init github.com/&lt;your_user&gt;/&lt;your_project&gt;

导入主题：
```toml
[module]
  [[module.imports]]
    path = &#34;github.com/hugo-fixit/FixIt&#34;
```
要更新或管理版本，你可以使用 hugo mod get 命令。
```shell
# 更新所有模块
hugo mod get -u
# 更新所有模块及其依赖
hugo mod get -u ./...
# 更新一个模块
hugo mod get -u github.com/hugo-fixit/FixIt
# 获取特定版本（例如 v0.3.2, @latest, @master, @dev）
hugo mod get github.com/hugo-fixit/FixIt@vdev
```
所以命令：
```shell
hugo new site blog
cd blog
hugo mod init blog
hugo mod get github.com/hugo-fixit/FixIt@dev
hugo server -D
```

---

> Author: [道数术科技](scdsskj.github.io)  
> URL: http://192.168.101.6:80/posts/12ab150/  

