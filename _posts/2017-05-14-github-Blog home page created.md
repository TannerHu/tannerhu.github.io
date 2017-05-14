---
layout:     post
title:      GitHub-博客搭建
date:       2017/5/14 21:22:30   
author:     Tanner Hu
summary:    新手GitHub搭建Blog
categories: jekyll
thumbnail:  cogs
tags:
 - GitHub
 - 博客主页创建
---
# 项目主页 #

在[GitHub][1]上建个账号后，在右上角点击**+**号，接着点**New repository**创建一个**Repository name**为**username.github.io**(username与你的注册用户名一致,这个就是你博客的域名了,等你注册了自己的域名后可以自定义域名)

![Thumper](http://wx4.sinaimg.cn/mw690/692c65a4gy1ffkyl57qgtj20qk0ke404.jpg)

弄好后在你建的这个**repo**下进入**Settings**子页下拉到**GitHub Pages**点击**Chose a theme**

![Thumper](http://wx4.sinaimg.cn/mw690/692c65a4gy1ffkz96u7slj20pi0bwmy0.jpg)

在跳转页面选好主题后点击**Select theme** 到这，一个项目主页就建好了，但是它是一个纯粹为项目推广准备的，因此并没有博客的结构。里面的内容可以在你刚建**repo**目录下的**index.md**里修改，主页地址就是**https://username.github.io/**

# 个人博客创建 #

在上节本地环境构建中下载并本地测试成功的现成模板改了配置文件**_config.yml**后是可以直接上传的，这些现成版模都有完整的的博客结构下面开始讲一些上传前的细节。

先下个文本编辑器推荐[Notepad++][2]轻便且功能强大。还要装一个用来上传同步**repo**的桌面软件[GitHub Desktop][3]。下载安装完毕后，用Notepad++打开之前测试版模根目录下的**_config.yml**文件把各种**Site settings**和**User settings**换成自己的资料没的话就先删了原来的空着先吧（baseurl: ""
url: https://**username**.githu.io 这两个必改的给出样板**username**用自己的不用再说了吧） 改完后在根目录下打开cmd执行：

    bundle exec jekyll serve

在浏览器里看下各种链接和信息是否变成自己改了的，有问题回去查，改了后回到**cmd**下按**Ctrl+c**先停止服务，然后再重新执行上面的代码，浏览器刷新重加载页面并检查。

都没问题了打开安装好了的**GitHub Desktop**用你的GitHub账号登陆。(需要注意的是，Github for Windows会帮你创建SSH Key，你打开邮件应该会收到邮件帮你创建SSH Key的信息，这也省了不少事)下面是软件界面简单介绍：

![Thumper](http://wx4.sinaimg.cn/large/692c65a4gy1ffl23pz4rrj216i0k9n34.jpg)

在右上角左侧点**+**号把你的GitHub上的**username.github.io**  克隆到本地，点击Clone后选择本地目录创建这个**repo**在你本地的文件夹。


![Thumper](http://wx4.sinaimg.cn/mw690/692c65a4gy1ffkz978017j20jq0kgt9i.jpg)

创建好后进入你选择的目录会有一个**username.github.io**的文件夹，把你刚刚测试好的现成版模根目录下的所有文件除了（**_site**文件夹还有**Gemfile**和**Gemfile.lock**文件）都复制和覆盖到**username.github.io**文件夹，复制完后
检查**username.github.io**里有没有**CNAME**文件里有别人家Blog地址的，有的话请一定要删干净，不然同步后GitHub会给你狂发邮件的，有**index.md**的话把文件删了。弄好后在**GitHub Desktop**点修改记录线最右侧最大的空心圆然后填Summary和Description再提交给master

![Thumper](http://wx4.sinaimg.cn/mw690/692c65a4gy1ffl5hcd0nvj20zk0kwwgb.jpg)

提交成功后画面如下然后再右侧最大的空心圆，最后点**Sync**就可以同步到你的GitHub的repo里了。

![Thumper](http://wx2.sinaimg.cn/mw690/692c65a4gy1ffl5hcp2vyj20zk0kwta1.jpg)

现在可以在浏览器里打开`https://username.github.io/`就看到你的博客了

文章一般在**_posts**文件夹里面的**.md**文件 你可以下载个[MarkdownPad][4]用来编写博文，按照现成版模里**.md**文件的样板编辑头信息，下面写文章写完保存在
你本地的**/username.github.io/_posts**目录下用**GitHub Desktop**上传到GitHub就可以在你的博客上看到了。（Notepad++基本可以打开现成版模里所有代码文件编辑，慢慢摸索吧，等熟悉了结构和语言你就可以自己写代码了～）

[1]: https://github.com/join?source=header-home
[2]: https://notepad-plus-plus.org/download/v7.3.3.html
[3]: https://desktop.github.com/
[4]: http://markdownpad.com/