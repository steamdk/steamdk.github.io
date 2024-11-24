## hugo 学习使用

### install
```
 CGO_ENABLED=1 go install -tags extended github.com/gohugoio/hugo@latest

 hugo new site blog


config.toml 文件包含了网站的配置信息，例如标题、语言、作者等。
archetypes 文件夹包含了新内容创建的模板文件，例如默认的 Markdown 文件。
content 文件夹包含了网站的内容，例如文章、页面等。
data 文件夹包含了网站的数据文件，例如 JSON 或 YAML 格式。
layouts 文件夹包含了网站的布局模板，例如首页、文章页面等。
static 文件夹包含了网站的静态文件，例如图片、CSS、JavaScript 等。
themes 文件夹包含了网站的主题，可以自定义网站的样式和布局。


下载主题

git submodule add https://github.com/dillonzq/LoveIt.git themes/LoveIt

或者

打开https://github.com/dillonzq/LoveIt ，点击 Code ，然后下载 ZIP ，再将文件解压至D:\Hblog\site_name\themes\LoveIt


 
.
├── archetypes # markdown文章的模版,包括文章前缀注释写法
├── config.toml # 配置文件
├── content # 网站内容，主要保存文章
├── data # 生成网站可用的数据文件，可用在模版中
├── layouts # 生成网站时可用的模版
├── public # 通过hugo命令生成的静态文件，这是我们网站真正要发布的目录
├── resources # 通过hugo命令一起生成的资源文件，貌似是临时文件
├── assets # 静态文件，比如文章中的图片/视频文件、css等, 将来其下的子目录和文件会在生成时候会自动复制到 public 目录中. 
├── static # 静态文件，比如favicon等图标, 以及site.xml等, 将来其下的子目录和文件会在生成时候会自动复制到 public 目录中. 
└── themes # 保存可用的hugo主题





1. 博客文章, 推荐放到 content/posts 子目录下
2. 全局性的静态文件, 比如 about.md 存储在 content 目录下
3. 博文图片, 推荐放在网站的 assets 目录下, 需要新建这个目录, 比如图片放到 assets\images
4. 音频文件, 推荐放到 assets\music 子目录下. 
5. 博文中引用的 css 样式, 推荐放到 assets\css 子目录下.
6. favicon 以及 andriod 下的图标和网站的一些 site.xml 推荐放到static 目录下.
7. 图标/图片/css如何引用?  比如 mkdown 文件如何引用图片? 
  hugo构建时候会将assets和static下的所有内容复制到 public 目录中, 所以mkdown 文件引用图片就可以使用下面的写法
   ![](/images/wechat.png)

```






### 配置参考github 有人在用这个主题写blog  https://github.com/YukiIsait/Blog/



### 写blog直接在 post 目录新建markdown文件 
- hugo new posts/000项目大纲.md

### 写完本地运行 启动 hugo server 预览
``` 
hugo server -D  --disableFastRender

   这个命令会完成文档生成, 并启动一个 live server, 默认端口是 1313, 使用浏览器打开 http://localhost:1313 预览。
   其中 -D 参数, 生成静态文件时是否包含 draft 博文.
   --disableFastRender 参数: 禁止hugo 会启用 hot reload 功能,  如在live reload 情况下, 一边修改文章一边可自动生成静态文件供预览, 很多时候比较烦人.
   hugo server -e production 命令用于生产环境的开启,
```


### 发布上线的话 
```
先将public目录清空
直接执行  hugo

默认情况下， hugo 将会将所有的内容发布到 hugo-blog\public 目录下，包括所有的img、js、css等等， 我们只需要将 public 目录发布到远端服务器上即可。当然， 我们也可以在 hugo-blog\config.toml 文件中增加 publishDir 变量来修改发布路径， 比如设置：  publishDir = "docs"
```


