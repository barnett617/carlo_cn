## 问答

#### 问: 在已经有了 Electron 和 NW.js 的情况下这个项目背后的动机是什么?

- 这个项目其中的一个动机是演示本地安装的浏览器是如何用来和箱外的Node进行配合的
- 在Carlo中 Node v8 和 Chrome v8 引擎是不挂钩的，因此就提供了一个拥有可独立更新底层组件的可维持的模型。Carlo在打包方面给与用户控制权，并且更注重生产化多于品牌化。

#### 问: 一个使用Carlo的Node应用可以被打包成一个桌面应用吗?

[pkg](https://github.com/zeit/pkg) 项目可被用来把一个Node应用打包为一个桌面应用。Carlo本身不提供品牌化配置能力，比如应用图标或定制菜单，取而代之的Carlo聚焦于生产和Web和Node之间的互相操作性。查看 [systeminfo](https://github.com/GoogleChromeLabs/carlo/tree/master/examples/systeminfo) 例子并调用 `pkg package.json` 看看它是怎么工作的。

#### 问: 如果用户没有安装谷歌浏览器会发生什么?

当定位不到谷歌浏览器时 Carlo 会打印出一条错误信息。

#### 问: Carlo支持的谷歌浏览器最低版本是?

谷歌稳定版系列，70.*的版本都被支持


