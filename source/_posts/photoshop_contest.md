title: Ps 大赛进行时 + 用 Python 在局域网内共享文件的方法
date: 2014-06-15
categories: 
- 活动
- 比赛
tags:
- Ps
- 网络
- Python
description: 灵动计算机社举办的 Photoshop 平面设计大赛的比赛现场。
keywords: Ps,Photoshop,平面设计大赛,平面设计
---

### Photoshop 平面设计大赛进行时

今天下午，“我爱一中”·Photoshop 平面设计大赛在信息楼语音室中开赛了，得到了不少同学的支持，共有 23 名选手参加了比赛。下面上图：

![灵动计算机社 Photoshop平面设计大赛 比赛现场](http://cptsct.qiniudn.com/photoshop_contest/3.jpg?imageView/2/w/680)

<!-- more -->

![灵动计算机社 Photoshop平面设计大赛 比赛现场](http://cptsct.qiniudn.com/photoshop_contest/2.jpg?imageView/2/w/680)

![灵动计算机社 Photoshop平面设计大赛 比赛现场](http://cptsct.qiniudn.com/photoshop_contest/1.jpg?imageView/2/w/680)

小编当时没能参加到这场比赛，没机会玩 Ps（快来安慰我 T_T）。所以，小编只好事后 P 了一下上面几张图片补偿一下，要是不小心 P 丑了，请不要打我。

---

### 用 Python 在局域网内共享文件

那小编当时到底干嘛去了呢？其实只有一件重要的事：“传文件!”

要知道，我们提供的素材包将近半G啊，又没有提前拷贝好。怎样在短时间内将这个大文件传到二十多台电脑上对我们来说是个不小的考验。用 U 盘复制？U 盘不够多呀，而且速度不快。看在语音室电脑的网卡还不错的份上，我们决定架设一个 HTTP 服务器，用内网来传输，让同学们用浏览器下载。

不过，架设 HTTP 服务器不是一件轻松的事情，需要一定的时间来配置。可我们得尽快呀，因为参赛的同学们已经陆陆续续地来到了！幸好我们早有准备，那就是—— Python 的 `SimpleHTTPServer`。

小编在此分享一下这个用 Python 在局域网内共享文件的方法吧（事实上，这个方法对于外网也是可以的，不过貌似没有什么优势）：

- __先装个 Python 2.x 的最新版__
Tips: Linux 系统中都通常预装 Python，一般可以跳过这步
 1. 下载选择与系统相应的版本：[python.org/downloads](https://www.python.org/downloads/)
 2. 安装的时候记得把可执行文件的目录添加到环境变量 `path` 里（Windows 系统下的设置方法如图），这样可以方便后面的操作。

![Add python.exe to Path](http://cptsct.qiniudn.com/photoshop_contest/python_installation_set_path.png?imageView2/2/format/jpg)

- __在命令行中定位到要共享的目录__
例如，在 Windows 中，要定位到 D:\Path\To\Your\Dir\，需要：
 1. 打开命令提示符，输入 `D:` 并回车，就定位到 D 盘的根目录了；
 2. 输入 `cd Path\To\Your\Dir` 并回车，就定位好了。

- __用 Python 共享这个文件夹__
在刚才那个完成定位的命令提示符窗口中，运行
		python -m SimpleHTTPServer 80
然后，在本机访问 <http://127.0.0.1/> 就可以看到效果了，而局域网中的其他设备要访问时，只需要把上面的 `127.0.0.1` 改成这台机子的内网 IP 即可。如果该目录中有 `index.html` 文件，则默认会展示这一文件；如果没有，则会显示一份文件列表，如图所示：

![Python SimpleHTTPServer 生成的文件列表](http://cptsct.qiniudn.com/photoshop_contest/filelist.png?imageView2/2/format/jpg)
上面的命令中，`80` 表示的是端口。当然，也可以用其他的端口，不过，访问的时候就要记得加上端口号，例如 <http://127.0.0.1:8000/>。

小编觉得，这个在内网共享文件的方法不算复杂吧。希望对你有所帮助。