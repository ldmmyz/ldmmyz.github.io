title: LingDong openSUSE - 为灵动而定制
date: 2014-05-03
categories: 分享
tags:
- 操作系统
- Linux
- 新鲜玩意儿
description: LingDong openSUSE，为灵动计算机社定制的 Linux 桌面系统。
---

喜欢尝新的同学们，来体验一下 LingDong openSUSE 吧。

这是子勤为灵动计算机社定制的一款 Linux 桌面系统，基于 [openSUSE 13.1](http://software.opensuse.org/131/zh_CN) i686，使用 [SUSE Studio](https://susestudio.com/) 构建，简体中文界面。

<!-- more -->

### 搭载软件包括：

* 内核：[Linux Kernel](https://www.kernel.org/) 3.11
* 桌面环境：[KDE](http://www.kde.org/) 4
* 浏览器：[Mozilla Firefox](https://www.mozilla.org/zh-CN/firefox/new/) 28
* 办公软件：
 - [WPS Office for Linux](http://linux.wps.cn/) Alpha 12 p4
 - [Okular 文档查看器](http://okular.kde.org/)
* 多媒体：
 - [VLC 播放器](http://www.videolan.org/vlc/) (及各种解码器) (可播放大多数常见视频格式)
 - [FFMPEG](http://www.ffmpeg.org/) (强大的编/解码器)
 - Flash Player
* 开发工具：
 - [GCC](http://gcc.gnu.org/) 4.8
 - [Free Pascal](http://www.freepascal.org/) 2.6.4
 - [Go](http://golang.org/)
 - [GDB](http://www.sourceware.org/gdb/)
 - [Vim](http://www.vim.org/) 文本编辑器
 - [Git](http://git-scm.com) 版本控制管理软件
 - [Indent](http://www.gnu.org/software/indent/) C代码风格转换工具
 - [Python](https://www.python.org/) 2.7
* 其他工具：
 - [Fcitx](https://code.google.com/p/fcitx/) 中文输入法
 - [Ark](http://www.kde.org/applications/utilities/ark/) 存档工具 (支持 tar, gzip, bzip2, zip, 7z, rar 等格式的解压缩)
 - [KTorrent](http://www.kde.org/applications/internet/ktorrent/) 点对点下载工具
 - [GParted](http://gparted.org/) 磁盘分区管理工具
 - [SuSE Studio 镜像写入器](http://software.opensuse.org/package/imagewriter)

这个系统能够满足许多场合的需求，不过，想用它玩游戏的孩子可能会受到打击。小编觉得，它挺适合搞 OI 的同学。

### 下载
下载 LingDong openSUSE 13.1.i686-0.0.9：<http://pan.baidu.com/s/1kT3FsiF>

### 使用方法

##### 1. 将 ISO 镜像烧入光盘或者写入 U 盘中

这里介绍一下写入将 LingDong openSUSE 镜像写入 U 盘的方法。

***注意：以下操作会删除 U 盘上原有的数据，请做好备份工作。***

* 在 Linux 系统中，我们可以用 `dd` 命令把它写入 U 盘：


	# umount /dev/sdX
	# dd if=/镜/像/路/径/文件名.iso of=/dev/sdX bs=4M

上面的命令请以 `root/sudo` 权限执行，其中的 `sdX` 请用你的 U 盘的实际标志代替，`/镜/像/路/径/文件名.iso` 请用所下载的文件的实际路径名代替。我们需要确保 U 盘未被挂载，即 `umount /dev/sdX`，才能执行 `dd` 命令。

* 在 Windows 系统中，我们可以用 SuSE Studio 镜像写入器把它写入 U 盘。

首先，下载 SuSE Studio 镜像写入器：<https://github.com/downloads/openSUSE/kiwi/ImageWriter.exe>
然后，把 LingDong openSUSE 镜像的扩展名由 `iso` 改为 `raw`	
接着，以管理员权限运行 `ImageWriter.exe`，按照界面提示操作即可把镜像写入 U 盘。

##### 2. 用上面制作好的介质启动电脑

这一步的操作方法在不同的机器上会有所不同，所以，请善用[搜索](http://www.lmgtfy.com/?q=%E4%BB%8EU%E7%9B%98%E5%90%AF%E5%8A%A8)。

### 尽情享受吧

登录 LingDong openSUSE 的时候，会提示输入用户名和密码：

用户名：cptsct
密码：cptsct

用户名：root
密码：linux

一般情况下，请使用 `cptsct` 用户登录。 (觉得很难记？其实就是 ComPuTer SoCieTy)

也许，你刚开始使用它的时候会有些不习惯，但如果能坚持尝试的话，你会发现，LingDong openSUSE 也是非常优雅地使用的。希望 LingDong openSUSE 能成为引导你踏入 Linux 世界的第一步。

你甚至还可以把这个系统安装到硬盘上，安装方法请自行探索。对于安装 Linux 系统缺乏经验的同学，请做好心理准备，小心，小心，再小心点哦。

-----

希望同学们能在下面的评论框里写下你对 LingDong openSUSE 的想法，以便我们能够不断改进它。
小编先来一条：未整合截屏工具