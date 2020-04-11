# 基于Next7主题美化的Hexo博客主题

![](https://img.shields.io/badge/Next-7.7.2-green.svg) 

> 本项目由许多借鉴[Sanarous](https://bestzuo.cn/)的地方，在此表示感谢！[欢迎访问我的博客](https://iluis.cn/)，点击蓝色字体即可进入！

- 在[CSDN](https://blog.csdn.net/qq_39720594)上有整理Hexo的搭建、部署、自定义域名以及优化细节的文章，欢迎大家阅读！

- 点击获取[Next主题最新版本](https://theme-next.org/)!

⚠️ 注意并不能保证网站的样式与本仓库中样式一致，如果你会修改 CSS 样式的话，可以继续在此基础上魔改 Next 主题。

## 使用方法

使用 GitBash，进入到本地 hexo 根目录，使用以下命令

```shell
git clone https://github.com/iluis97/hexo-theme-next7.git /themes/hexo-themes-next7
```

其中`/themes/hexo-themes-next7`名称可以任取，只要放到 hexo 下的 themes 主题下即可。

## 配置文件准备

hexo 站点根目录下配置，供参考：

```yml
# Hexo Configuration
## Docs: https://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/

# Site
title: iluis
subtitle: 一个热爱开发的技术小白
description: 本站主要是分享一些Java知识，以及博客的搭建技巧，欢迎来访呀！
keywords: Iluis,Java,Hexo,Next,个人博客,hexo博客
author: iluis
language: zh-CN
timezone: Asia/Shanghai

# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: https://iluis.gitee.io/ #绑定域名
root: / #默认根路径，指向实际的source
permalink: :year/:month/:day/:title/
permalink_defaults:
pretty_urls:
  trailing_index: true # Set to false to remove trailing 'index.html' from permalinks
  trailing_html: true # Set to false to remove trailing '.html' from permalinks

# Directory
source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
skip_render: README.md # 部署的时候不包含的文件

# Writing
new_post_name: :title.md # 默认的新博文名称
default_layout: post # 默认布局
titlecase: false # Transform title into titlecase
external_link:
  enable: true # Open external links in new tab
  field: site # Apply to the whole site
  exclude: ''
filename_case: 0 #把博客名称改成小写/大写（1,2）
render_drafts: false # 是否显示草稿
post_asset_folder: true #是否启用资源文件夹（用来存放相对路径图片或文件）
relative_link: false # 把链接改为与根目录的相对位址
future: true
highlight:
  enable: true #是否开启代码高亮
  line_number: true #是否增加代码行号
  auto_detect: true #自动判断代码语言
  tab_replace: ''
  wrap: true
  hljs: false
  
# hexo-neat 博文压缩
neat_enable: false

neat_html:
  enable: true
  exclude:
  
neat_css:
  enable: true
  exclude:
    - '*.min.css'

neat_js:
  enable: true
  mangle: true
  output:
  compress:
  exclude:
    - '*.min.js'  

# Home page setting
# path: Root path for your blogs index page. (default = '')
# per_page: Posts displayed per page. (0 = disable pagination)
# order_by: Posts order. (Order by date descending by default)
index_generator:
  path: ''  #博客的默认路径
  per_page: 10  #每页博客数量上限
  order_by: -date  #博客排序

# Category & Tag
default_category: uncategorized
category_map:
tag_map:

# Metadata elements
## https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta
meta_generator: true

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
date_format: YYYY-MM-DD #博客日期格式
time_format: HH:mm:ss #博客时间格式
## Use post's date for updated date unless set in front-matter
use_date_for_updated: false

# Pagination
## Set per_page to 0 to disable pagination
per_page: 10
pagination_dir: page

#归档页的分页设置
archive_generator: #归档页的配置
  per_page: 30 #归档页每页博客数
  yearly: true #按年归档
  monthly: true #按月归档
#标签页的分页设置
tag_generator:
  per_page: 20 #标签页每页博客数

# Include / Exclude file(s)
## include:/exclude: options only apply to the 'source/' folder
include:
exclude:
ignore:

# Extensions
## Plugins: https://hexo.io/plugins/
plugins: hexo-generate-feed #设置rss订阅
## Themes: https://hexo.io/themes/
theme: next7
# 搜索
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
# 统计数据
symbols_count_time:
  symbols: true #是否统计字数
  time: true #是否统计阅读时长
  total_symbols: true #是否统计总字数
  total_time: true #是否统计总阅读时长
# 音乐插件  
aplayer:
  meting: true

live2d:
  enable: true
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: false
  debug: false
  model:
    use: live2d-widget-model-shizuku
  display:
    position: right
    width: 150
    height: 300
  mobile:
    show: false 

# Deployment
deploy: #博客部署
  type: git
  repo: # 仓库路径
       https://github.com/iluis97/hexo-theme-next7.git
```

### 启动hexo博客

- hexo clean、hexo g、(gulp：压缩命令)、hexo s、hexo  d
