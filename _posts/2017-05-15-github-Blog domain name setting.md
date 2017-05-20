---
layout:     post
title:      GitHub-博客域名设置（4）
date:       2017/5/15 18:00:16    
author:     Tanner Hu
summary:    新手GitHub搭建Blog
categories: jekyll
thumbnail:  cogs
tags:
 - GitHub
 - 博客
 - 域名设置
---
# 设置自己的域名 #

首先得要注册个自己的域名，这里推荐几个域名注册平台，非常热门的 [Godaddy][1] 很适合新手，支持国内的支付宝支付，刚开始新注册用优惠码有不小力度的优惠，但是到期后续费价格就略坑了，续费的优惠码也少。国内的 [万网][2] 价格真的是非常棒！只是国内的网址备案政策流程要走20多天... 下面列些国外比较热门域名平台（知道的不多，我也只是刚建博客有兴趣的去多了解下吧我自己用的是Godaddy毕竟热门资料多，等要续费时转namesilo价格看起来挺不错的） [美国域名中心][3] ; [name][4] ; [namecheap][5] ; [namesilo][6] ; [pananames][7] ;

注册好域名后，先到 GitHub 的 **username** .github.io目录下新建个名字为 **CNAME** 的文件，里面输入刚注册的一级域名例如我的是 `haxbk.com` 然后点提交更改给 master 支线。

Godaddy 默认用的 DNS 解析貌似被墙了，所以要把域名的 DNS 解析交给国内的服务器，我这里推荐用国内免费的 [DNSPOD][8] 可以用QQ登陆具体操作步骤可以参考 [如何使用dnspod解析域名][9] ，添加记录里的 **记录值** 就用你**username**.github.io 当然前面要选采用CNAME记录，相比用A记录的有CDN加速。

上面弄好后去 [Godaddy][10] 找到管理域名点进去

![Thumper](http://wx1.sinaimg.cn/large/692c65a4gy1ffmbs3w4o3j20xm0awwfe.jpg)

然后再点域名小版面右上角小齿轮里的管理DNS 

![Thumper](http://wx3.sinaimg.cn/large/692c65a4gy1ffmbs32p81j20f707s3yo.jpg)

 在域名服务器栏点更改,把刚刚在 DNPOD 添加记录时,那两个记录类型是NS不能更改的记录值填进去保存就可以了(`f1g1ns1.dnspod.net`和`f1g1ns2.dnspod.net`)

![Thumper](http://wx4.sinaimg.cn/large/692c65a4gy1ffmbs3nbzoj20ky07mq36.jpg)

DNSPOD 解析的设置不是立即生效的，等10分钟左右用新设置的域名进博客试试~ 

[GitHub上博客的搭建-前言（1）][11] ; [GitHub上博客的本地环境构建（2）][12] ; [GitHub-博客搭建（3）][13] ; [GitHub-博客域名设置（4）][14] ; [GitHub-建站的实用工具站推荐（5）][15]

[1]: https://sg.godaddy.com/
[2]: https://wanwang.aliyun.com/
[3]: http://www.usdomaincenter.com/
[4]: https://www.name.com/
[5]: https://www.namecheap.com/
[6]: https://www.namesilo.com/
[7]: https://www.pananames.com/
[8]: https://www.dnspod.cn/Login?r=/console/dns
[9]: https://jingyan.baidu.com/article/546ae1857c4ee81149f28cbe.html
[10]: https://sg.godaddy.com/
[11]: /jekyll/2017/05/11/guithub-Blog-to-build-preface/
[12]: /jekyll/2017/05/13/github-Blog's-local-environment/
[13]: /jekyll/2017/05/14/github-Blog-home-page-created/
[14]: /jekyll/2017/05/15/github-Blog-domain-name-setting/
[15]: /jekyll/2017/05/20/github-Tool-site/
