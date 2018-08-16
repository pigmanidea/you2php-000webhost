# 教你如何免费部署You2php，可实现“长城”内观看油管视频。
作者：pigmanidea.
[免翻墙看Youtube教程]
# 什么是You2php?
You2PHP是一个用PHP开发的Youtube流量代理脚本、通过对接谷歌api获取数据，可用来搭建Youtube视频镜像站、可实现长城之内观看Youtube。
详情官网：https://you2php.github.io
免翻墙：https://github.com/You2php/you2php/
# 编写缘由：
YouTube上面也有you2php的教程，小编试着按步骤走，后来觉得使用不太理想，具体几个缺点：1.网页速度慢，不超过500kb/s。2.下载视频容易中断或者失败。3.会被主机商停用7个小时。
小编试着使用自己方式部署You2php,发现观看油管视频的网速胜过免费的vpn,ssr,v2ray等免费翻墙节点，下载视频速度正常保持1M/S。使用一个月以来，还未出现被主机商停用的情况，除了偶尔网速上不去，正常时候都能流畅得播放视频。
# 关于学习部署You2php的申明：
1.	敏感人士不要使用，学习人士低调使用，请不要广泛传播；
2.	小编拒绝商业用途，拒绝帮别人搭建You2php并收取报酬 https://github.com/You2php/you2php/
3.	伸手党请绕道，本项目需要耐心按照教程步骤才能成功；
4.	请不要将此教程拿去谋取利益，一切因商业用途产生的法律问题一律与Pigman无关，也给广大好友提个醒，花钱委托别人帮忙很容易泄露自己隐私，有可能被别人盗取信息使用。
# 简单原理：
我是将You2php部署在000webhost的海外免费虚拟主机上，绑定自己免费域名，再通过cloud flare进行DNS免费加速，实现看油管视频的。000webhost为每个free app提供10G/月的流量，所以还得省点使用。
# 具体部署：
# 1.准备梯子：
因为部分网页的账户注册，还有youtube api的获取，需要梯子才能进行。请有代理的人士可以跳过这一步骤，没有先暂时使用下面链接的作者的方法吧。（注意：对宗教敏感的人士请不要使用，里面的软件都涉及到宗教信息，想搭梯子请另找他路吧。）https://github.com/bannedbook/fanqiang/wiki

获取Youtube API：请查看教程 https://laod.cn/tools/you2b-php.html

获取you2php的源码：下载压缩包 https://zhujiwiki.com/12297.html 或者 https://github.com/pigmanidea/you2php-000webhost/blob/master/you2php.zip

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/1.png)
# 2.申请免费域名：
该过程需要梯子。请访问网站链接：https://www.freenom.com/zh/index.html?lang=zh
第一步：注册一个账户。
![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/2.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/3.png)

使用谷歌邮箱登陆。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/4.png)

我们要创建一个免费域名。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/5.png)

查找域名，比如：pigman

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/6.png)

任意选择一个，都是免费的。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/7.png)

点击“checkout”。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/8.png)

点击购买12个月。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/9.png)

打沟，其他信息可以不填，然后直接下一步。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/10.png)

已经购买成功，跳回主页。

# 3.申请000webhost账号，获得免费虚拟主机。
请登录网址 https://www.000webhost.com/ 注册时候需要梯子。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/11.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/12.png)

这一步应该不难吧？注册完成后要验证邮箱地址，查看Email，验证000webhost的注册地址，即可申请成功。邮件的收到可能需要一点时间，请耐心等待几分钟。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/13.png)

申请成功，进行登陆。Log in.


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/14.png)

点击管理，因为它已经为我们创建一个免费app了，所以可以开始进行you2php的上传。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/15.png)

点击上传。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/16.png)

进去看到这个界面，将htaccess这个文件删除，否则播放视频会出现错误。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/17.png)

单机右键，删除。
有时候网页会要我们重新登陆，你可以重新再进去，或者再登陆000webhost.


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/60.png)


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/18.png)


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/19.png)

上传文件

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/20.png)

这个界面表示，上传文件成功。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/21.png)

我们要把它解压出来。并重命名，比如：2018。“2018”文件夹作为空间的根目录。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/22.png)

可以将压缩包删除了。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/23.png)

进入我的“2018”的文件里，看到“you2php”,再点进去，将里面文件移出来。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/24.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/25.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/26.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/27.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/28.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/29.png)

即可看到此列表。

接下来，将“2018”文件加锁。因为不加锁容易被GFW封锁，可能被别人盗取信息，比如你的YouTube api。下面进行演示：
![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/30.png)
![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/31.png)
![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/32.png)
![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/33.png)

选择自己要加锁的文件夹，设置用户名和密码。

绑定自己的域名：

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/34.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/35.png)
![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/36.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/37.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/38.png)

添加自己的域名


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/39.png)

复制这行字。接下来到刚刚买域名的网站进行绑定。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/40.png)

登陆，选择 my domains.



![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/41.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/42.png)

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/43.png)

按格式填写。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/44.png)

成功绑定域名。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/45.png)

回到000webhost检查，域名是否连接我的app了，这一过程请等5分钟。跳不出来请重新登陆000webhost,检查。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/46.png)

000webhost收到响应了，我们需要link它。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/47.png)

最后的连接步骤

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/48.png)

连接成功的界面。

5.	进行DNS加速。
注册cloudflare.账号， https://dash.cloudflare.com/sign-up
注意这一步骤必须先使域名成功绑定000webhost后，才能继续进行这一步。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/49.png)

按要求填写，验证邮箱，即可成功。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/50.png)


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/51.png)

添加要加速的域名。


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/52.png)

点击下一步


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/53.png)

选择免费项


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/54.png)

点击继续


![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/55.png)

先复制第一项，再复制第二项，将上面的两行地址，和刚刚申请域名的界面里进行替换。如下图：

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/56.png)

回到cloudflare，点击继续，等10几分钟，当你看到下面的绿色条纹，即连接成功。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/57.png)

好了，现在可以说离成功只差最后一步了。

# 6.You2php的安装:
请使用火狐浏览器或者谷歌浏览器登陆你的you2php。个人测试，国产的浏览器观看速度很慢，甚至出现视频播放失败的状况。请使用国外浏览器观看。
进入你的you2php，请在域名后面加上文件名，也就是放you2php的空间根目录，比如“/2018”，我的是这个(https://pigman.ml/2018)。这里面一个小细节：https与http,其中第一个会比较安全。一般建议你用https，然而我们部署完后，https协议得等一段时间才能生效，最晚24小时，你现在先用http协议吧。

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/58.png)

进去后要你输入你的用户名，密码。

接下来步骤，请按照这位作者的步骤填写吧：https://laod.cn/tools/you2b-php.html

![Alt text](https://github.com/pigmanidea/you2php-000webhost/raw/master/images/59.png)

认真填写，点击继续，安装完成后，即可观看啦。


