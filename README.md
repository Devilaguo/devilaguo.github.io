## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Devilaguo/devilaguo.github.io/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Devilaguo/devilaguo.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact# Hexo-Theme-NexT主题配置

 2020-08-02 2020-08-03 [教程](https://jakelin.cn/categories/教程/) 867

 5.4k 5 分钟

由于个人感觉，找图片困难（有选择困难症......），虽然使用了图床，但是原本使用的Butterfly主题需要配置图片让我有点难受（是我太菜了）。现在切换为最新的NexT主题，记录当前主题配置。

2020-08-02 版本信息

> nodejs : v12.18.3
>
> hexo: 5.0.0
> hexo-cli: 4.1.0
>
> NexT : [v8.0.0-rc.5](https://github.com/next-theme/hexo-theme-next/releases/tag/v8.0.0-rc.5)

# 预览

[![Next主题首页截图.png](https://i.loli.net/2020/08/03/IFlo6fVkXJ8HpUv.png)](https://i.loli.net/2020/08/03/IFlo6fVkXJ8HpUv.png)

[Next主题首页截图.png](https://i.loli.net/2020/08/03/IFlo6fVkXJ8HpUv.png)



[![Next主题博客界面截图.png](https://i.loli.net/2020/08/03/X1WITxsLjgeuSpK.png)](https://i.loli.net/2020/08/03/X1WITxsLjgeuSpK.png)

[Next主题博客界面截图.png](https://i.loli.net/2020/08/03/X1WITxsLjgeuSpK.png)



# 获取Next

```
git clone https://github.com/next-theme/hexo-theme-next themes/next
```

# 站点配置文件

根目录 `_config.yml`

```
theme: next
```

# Next主题配置

## 主题配置文件

将主题配置文件放在 `网站很目录` 下，命名为 `_config.next.yml` ，详情见：[Configuration](https://theme-next.js.org/docs/getting-started/configuration)

```
cp themes/next/_config.yml ./_config.next.yml
```

## 选择主题风格

```
# Schemes
#scheme: Muse   #预览参考 https://theme-next.js.org/muse/
#scheme: Mist     #预览参考 https://theme-next.js.org/mist/
#scheme: Pisces #预览参考 https://theme-next.js.org/pisces/
scheme: Gemini  #预览参考 https://theme-next.js.org/
```

## 菜单

```
menu:
  首页: / || fa fa-home
  归档: /archives/ || fa fa-archive
  分类: /categories/ || fa fa-th
  标签: /tags/ || fa fa-tags
  
menu_settings:
  icons: true # 显示图标
  badges: true # 显示统计信息
```

### 添加标签页面

生成编辑`Hexo/source/tags/index.md`

```
---
title: 标签
date: 2020-07-29
type: tags
comments: false
---
```

### 添加分类页面

生成编辑`Hexo/source/categories/index.md`

```
---
title: 分类
date: 2020-07-29
type: categories
comments: false
---
```

## 头像设置

```
# Sidebar Avatar
avatar:
  # Replace the default image and set the url here.
  url: https://i.loli.net/2020/07/31/OZl2JxuSRrweIk5.jpg #/images/avatar.gif
  # If true, the avatar will be dispalyed in circle.
  rounded: true  
  # If true, the avatar will be rotated with the cursor.
  rotated: false
```

## 网站图标

```
# Favicon（网站图标）
favicon:
  small: https://i.loli.net/2020/07/31/OZl2JxuSRrweIk5.jpg
  medium: https://i.loli.net/2020/07/31/OZl2JxuSRrweIk5.jpg
  apple_touch_icon: https://i.loli.net/2020/07/31/OZl2JxuSRrweIk5.jpg
  safari_pinned_tab: https://i.loli.net/2020/07/31/OZl2JxuSRrweIk5.jpg
  #android_manifest: /images/manifest.json
  #ms_browserconfig: /images/browserconfig.xml
```

## 社交链接

```
social:
  GitHub: https://github.com/yourname || fab fa-github
  E-Mail: mailto:yourname@gmail.com || fa fa-envelope

social_icons:
  enable: true      # 显示社交图标
  icons_only: true  # 只显示图标，不显示文字
  transition: false
```

## 首页显示的文章属性

```
post_meta:
  item_text: false # 设为true 可以一行显示，文章的所有属性
  created_at: true
  updated_at:
    enable: true   # 显示修改的时间
    another_day: false # 设true时，如果创建时间和修改时间一样则显示一个时间
  categories: true  # 显示分类信息
```

## footer信息

```
footer:
  # Specify the date when the site was setup. If not defined, current year will be used.
  since: 2019
  icon:
    name: fa fa-user
    animated: false
    color: "#808080"

  copyright: false
  # Powered by Hexo & NexT
  powered: true
```

## 目录设置

```
toc:
  enable: true
  # Automatically add list number to toc.
  number: true
  # 如果为true，则所有标题将在标题宽度长于边栏宽度的情况下放在下一行。
  wrap: false
  # 如果为true，则将显示帖子中所有级别的TOC，而不是帖子中已激活的部分。
  expand_all: true
  # Maximum heading depth of generated toc.
  max_depth: 6
```

## 打赏

```
reward_settings:
  # If true, reward will be displayed in every article by default.
  enable: true 
  animation: false  # 字体转动 鬼畜。。。。
  #comment: Donate comment here.

reward: # 打赏二维码链接
  wechatpay: https://i.loli.net/2020/08/01/na8BbXF1ow63OIJ.png 
  alipay: https://i.loli.net/2020/08/01/NALchOTe3vM8aYy.jpg
```

## 文章版权声明

```
creative_commons:
  license: by-nc-sa
  sidebar: true
  post: true
  language:
```

## 代码块

```
codeblock:
  # Code Highlight theme
  # All available themes: https://theme-next.js.org/highlight/
  theme:
#    light: default
#    dark: tomorrow-night
    light: atom-one-dark-reasonable
    dark: atom-one-dark-reasonable
  prism:
    # light: prism
    # dark: prism-dark
    light: prism-vsc-dark-plus
    dark: prism-vsc-dark-plus
  # Add copy button on codeblock
  copy_button:
    enable: true # 复制按钮的开关
    # Available values: default | flat | mac
    style: mac
```

## GitHub_Banner

```
github_banner:
  enable: true
  permalink: # 你的GitHub地址
  title: Follow me on GitHub
```

## 配置本地搜索

安装插件：

```
npm install hexo-generator-searchdb --save
# Local Search
# Dependencies: https://github.com/theme-next/hexo-generator-searchdb
local_search:
  enable: true
  # If auto, trigger search by changing input.
  # If manual, trigger search by pressing enter key or search button.
  trigger: auto
  # Show top n results per article, show all results by setting to -1
  top_n_per_article: 1
  # Unescape html strings to the readable one.
  unescape: false
  # Preload the search data when the page loads.
  preload: false
```

## busuanzi统计

安装插件：

```
npm install hexo-wordcount --save
busuanzi_count:
  enable: true                     # 设true 开启
  total_visitors: true             # 总阅读人数（uv数）
  total_visitors_icon: fa fa-user  # 阅读总人数的图标
  total_views: true                 # 总阅读次数（pv数）
  total_views_icon: fa fa-eye      # 阅读总次数的图标
  post_views: true                  # 开启内容阅读次数
  post_views_icon: fa fa-eye       # 内容页阅读数的图标
```

## 字数统计、阅读时长

安装插件：

```
npm install hexo-word-counter --save
# Post wordcount display settings
# Dependencies: https://github.com/next-theme/hexo-word-counter
symbols_count_time:
  separated_meta: true # false会显示一行
  item_text_post: true # 显示属性名称,设为false后只显示图标和统计数字,不显示属性的文字
  item_text_total: true # 底部footer是否显示字数统计属性文字
```

# 自定义样式

首先在 NexT 的配置文件 `_config.next.yml` 中取消下列对应样式文件的注释：

```
custom_file_path:
  #head: source/_data/head.swig
  #header: source/_data/header.swig
  #sidebar: source/_data/sidebar.swig
  #postMeta: source/_data/post-meta.swig
  #postBodyEnd: source/_data/post-body-end.swig
  #footer: source/_data/footer.swig
  #bodyEnd: source/_data/body-end.swig
  #variable: source/_data/variables.styl
  #mixin: source/_data/mixins.styl
  #style: source/_data/styles.styl
```

## 背景图片

取消 `_config.next.yml` 中 `style: source/_data/styles.styl` 注释。

创建 `source/_data/styles.styl` ：

```
// 设置背景图片
body {
    # 图片地址
    background:url(https://i.loli.net/2020/08/02/pjAgE9dIcTZSCoB.jpg); 
    background-repeat: no-repeat;
    background-attachment:fixed; //不重复
    background-size: cover;      //填充
    background-position:50% 50%;
}
```

## 设置透明度

`source/_data/styles.styl` 中增加样式：

```
//博客内容透明化
//文章内容的透明度设置
.content {
  opacity: 0.85;
}

//侧边框的透明度设置
.sidebar {
  opacity: 0.8;
}

//菜单栏的透明度设置
.header-inner {
  background: rgba(255,255,255,0.85);
}

//搜索框（local-search）的透明度设置
.popup {
  opacity: 0.85;
}

// sidebar css 
.sidebar{
    background-color:transparent;
}
```

## 圆角设置

取消 `_config.next.yml` 中 `style: source/_data/variables.styl` 注释。

创建 `source/_data/variables.styl` ：

```
// 圆角设置
$border-radius-inner     = 15px 15px 15px 15px;
$border-radius       
```

相关文章推荐

- 

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
