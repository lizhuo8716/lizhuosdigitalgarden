---
{"dg-publish":true,"dg-home":null,"Author":"dalizhuo","类型":["公众号文章"],"tags":["工具软件","工具软件/数字花园","工具软件/obsidian"],"备注":null,"permalink":"/2_兴趣_日记与留档/收集/基于Obsidian的个人数字花园/","dgPassFrontmatter":true}
---


# 前言：基于大佬的博客
[Obsidian-Digital-Garden (maxieewong.com)](https://garden.maxieewong.com/000.wiki/Obsidian-Digital-Garden/)
感觉很有意思啊，这样低成本满足自己分享欲的操作深得我心。马上开搞。
陌生名词很多，所以也在 B 站上找了找教程，真有一个：
[【Obsidian】人人都可以构建的 属于自己的独立网站 | Obsidian 发布、数字花园打造 | 渐进创作_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1HF411173m/?spm_id_from=333.337.search-card.all.click&vd_source=657e94a564f00cc09309946e94d463dc)

# 1. github 仓库的建立
git 注册（自己想办法） https://github.com/
Digital Garden 一键部署 https://dg-docs.ole.dev/advanced/hosting-alternatives/ 
![Pasted image 20240415075726.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020240415075726.png)


Digital Garden 插件设置（后期需要美化的参考就看下这里） https://dg-docs.ole.dev/getting-started/04-appearance-settings/ 
yaml 区设置（这一步好像全开就行） https://dg-docs.ole.dev/getting-started/03-note-settings/

具体操作步骤下面的知乎链接说得很好。我直接摘抄了：
网页： [利用Obsidian搭建自己的Digital Garden - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/677556713)
本地：[[[利用Obsidian搭建自己的Digital Garden \|[利用Obsidian搭建自己的Digital Garden ]]

# 2. 当建立好连接后发现，国内连不上，手机连不上 rua，得另外想办法。

需要结合下面两个文章：
[解决 Vercel 部署网站在国内被墙 | Zoey's Blog (blog-zoey.top)](https://blog-zoey.top/posts/vercel-dns-china)
[如何在国内访问vercel部署应用？ - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/666912903)

如果你了解 DNS 的 CNAME/A 记录，可以直接拿走下面的两行配置。
```
CNAME: name-china.vercel-dns.com
A: 76.223.126.88
```
Vercel 为墙内准备的贴心解析，二选一即可。出自[Vercel Incident History](https://www.vercel-status.com/history)。


## 2.1 准备条件

- 申请一个国内可访问的域名（新手可 1 元购于阿里云，`xyz`, `top` 这种后缀都是很便宜的）
-![Pasted image 20240415082349.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020240415082349.png)

- 注册 Cloudfare[随时随地连接、保护和构建 | Cloudflare (cloudflare-cn.com)](https://www.cloudflare-cn.com/)（为什么不用阿里云自带的DNS? 免费版不支持海外🚬）

1. 将准备好的国内域名加入 Cloudfare websites, 然后选择免费计划。![cloudfare-add-domain](https://blog-zoey.top/static/images/cloudfare-add-domain.png)
2. 点进该域名的配置面板，增加两条 DNS 配置。
![Pasted image 20240415082158.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020240415082158.png)


3. 接着往下滑，看到配置 Nameservers, 是 Cloudfare 给你准备好的，就是下面两个云右边的字符串，你得拿着这两个地址去换掉腾讯云（阿里云）原本的解析**：
   ![Pasted image 20240415082517.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020240415082517.png)
   3. 接下来是⌛️等待时间，Cloudfare 会给你发邮件的。
   4. 对部署好的 vercel 应用添加除了自带域名的新域名解析

进入到部署好了的项目的主页，可以看到一个“Domain”的按钮，点击进入：

![](https://pic2.zhimg.com/80/v2-0f4c6893783cdaba73050a122cbb7615_720w.webp)

然后进入之后，输入你买好的域名然后点击Add：

![](https://pic2.zhimg.com/80/v2-8052786687ff4888c58ebe1c487b8e29_720w.webp)

选择默认的方案，也就是把根域名和`www`解析一起加上。

![](https://pic4.zhimg.com/80/v2-ecded43097acb4f031101f724e3b2403_720w.webp)

添加之后会进行校验，校验完成了之后就可以进行访问了。。。**看起来是这样，实际上还是有问题的！！！**

### 四、Vercel + Cloudflare = 重定向次数过多解决方案

你把域名解析添加好了，校验也通过了，然后你会直接点击访问：

![](https://pic2.zhimg.com/80/v2-5a59b0726e58cad8dfbaefa3059fae95_720w.webp)

没错，你会遇到**重定向次数过多**的问题。

这其实是Cloudflare为添加的站点加密模式设置错误导致的。

进入 Cloudflare Dashboard，点击有问题的域名，打开左侧的 SSL/TLS 设置，在 Overview 中设置加密模式为完全或完全（严格）即可。

![](https://pic1.zhimg.com/80/v2-13f714c1543f459afab80973ba45dd60_720w.webp)

这样子之后你的`vercel`应用应该是可以正常的在国内进行访问了。

希望这篇文章能给大家在进行vercel部署的时候起到一些小小的帮助~！










