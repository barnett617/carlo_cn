# 概述

Carlo通过 \[Puppeteer\]\([https://github.com/GoogleChrome/puppeteer/\](https://github.com/GoogleChrome/puppeteer/%29\) 对象与本地安装的浏览器进行通信，并借助谷歌浏览器为Node应用提供渲染能力，同时还实现了Node和浏览器之间的远程调用。

###### ![](https://user-images.githubusercontent.com/883973/47826256-0531fc80-dd34-11e8-9c8d-c1b93a6ba631.png)我可以做什么?

用户使用Carlo可以创建兼并Web堆栈渲染和Node能力的混合应用：

* 对于Node应用，web渲染栈可以使用户可视化地看到应用的动态状态。
* 对于Web应用，通过访问Node将拥有更多的系统能力。
* 通过使用 \[pkg\]\([https://github.com/zeit/pkg\](https://github.com/zeit/pkg\)\) 可以将应用打包成一个单独的可执行包。

###### 它怎么工作的?

* Carlo定位到本地安装的谷歌浏览器。
* 启动Chrome并通过进程管道建立一个连接。
* 在Node环境中暴露出一个高级别API用于在Chrome中做渲染。



