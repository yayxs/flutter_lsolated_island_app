**那个固执的少年回来了** 《孤岛 App》这个系列已经停更了很久，这次全面升级，对的起给我`star` 的老铁们

## 介绍

> APP 名称：《独 °》
>
> 客户端方案：flutter
>
> 服务端方案：Koa2

### 功能

写着完善着

```sh
 - 我的
  - 个人信息
  - 头像修改
 - 首页
  - 列表页
  - 发送图文、视频等
 ……
```

### 前序准备

- _下文链接预警_
- _长文预警_
- _唠嗑方式不正经预警_

当开始全面更新迭代的时候，没有`产品` 的思维是多么可怕的一件事，开发的过程中会同步更新系列文章，希望一块`撩一撩flutter` **当然了这些文章都是没有更新的**

- [Flutter 实战 从头撸一个「孤岛」APP（No.1、项目初始化、屏幕适配）](https://juejin.im/post/5dd0142be51d453fc01e8a25)
- [Flutter 实战 从头撸一个「孤岛」APP（No.2、闪屏 Splash Page、引导页）](https://juejin.im/post/5dd97d3fe51d45234f582cbe)
- [Flutter 实战 从头撸一个「孤岛」APP（No.3、书单、搜索框、Dio 初探）](https://juejin.im/post/5de2b7aa5188256e913c991d)
- [Flutter 实战 从头撸一个「孤岛」APP（No.4、流行、点赞、动画）](https://juejin.im/post/5e12943f6fb9a0482806df9d)

### 分支变动

![20200315111241.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315111241.png)
是这样的，咱们把之前持续更新的移动到`lsolated_island_app` 这个分支。想要翻看的可以自行`clone` 《独》所有的开发现在`master` 分支。**可能旧的文档地址找不到的情况，这个我后续更新一下**

之前我的评论区

- 问：为啥 flutter 评论那么少
- 答：可能大家还不太了解

我觉得自己开发个小 app 也挺好玩的。

希望多多鼓励很关注，有不恰当的地方也欢迎指正。

> 友情建议：
>
> 最近一段时候由于公司需求，笔者在用 Vue 生态的 uniapp 技术栈来开发 app，总体体验是不太好的
>
> 不做什么横向对比，在正确使用 flutter 的前提下，flutter 开发的应用是相比于 uniapp 好很多的（这只是我个人看法）
>
> 个人感觉 flutter 的学习成本还是比较高的，如果公司想要通过这个技术来开发的话，可能需要有同事持续跟进 flutter 的生态发展，并定期分享给成员，因为 flutter 生态是越来越活跃，技术的更新迭代是相当的迅速，相关的第三方包插件今个能用。明天可能你就不知道咋回事了
>
> flutter 只是一个简单的 UI（这里特别说一下并没有所谓的嵌套问题），但是其在安卓 IOS 上的渲染能力，动画能力是十分的惊人
>
> 最后简单说一下，企业项目十分花里胡哨的话，可能生态中并没有良好的解决方案，这就需要改一些现有的源码，什么和开发者沟通我该怎么实现，这也为什么企业选择 taro uniapp rn 等等

### 数据分析

- 为什么有的人说 flutter 凉了吗
- 有的人说 2020flutter 你跳槽张薪资必备

**简单的数据说话**

| 多终端解决方案                                             | 星星数![img](file:///C:\Users\666\AppData\Local\Temp\SGPicFaceTpBq\12652\00252065.png) |     |
| ---------------------------------------------------------- | -------------------------------------------------------------------------------------- | --- |
| [_flutter_](https://github.com/flutter/flutter)            | 88.3K                                                                                  |     |
| [_react_-native](https://github.com/facebook/react-native) | 85.5K                                                                                  |     |
| [_taro_](https://github.com/NervJS/taro)                   | 24.3K                                                                                  |     |
| [uni-app](https://github.com/dcloudio/uni-app)             | 19K                                                                                    |     |

虽然`星星数` 并不能说明什么，但在技术选型的时候，它还是一个十分重要的参考价值，**笔者最近在做自己的全栈项目相信不久会出生吧**

也只好通过以文字的时候，敦促自己，其实想想`录视频也挺好的` 慢慢来吧

## BIOS 开启

由于简单配了台主机`flutter` 的运行需要 主机开启`BIOS` 模式

1.  开机快速按`f12`或者`DEL` 也就是删除键 进入 BIOS（不同的电脑型号是不尽相同的）
2.  先不切换语言模式（一般情况下默认是 english）点击 Advanced Mode（F7）进入高级选项。
3.  点击 Advanced，然后点 CPU Configuration。
4.  下拉菜单找到 Intel Virtualization Technology，在其子菜单下把选项改成 Enabled。
5.  按 F10 保存退出，开启成功。
6.  这样一般就可以成功重启了

至于想我这样，多快的手速都进不去`BIOS` 的人，那可能需要简单的拆一下`显卡` 然后再简单的卸载一下`主板的电池`  
![20200315111008.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315111008.png)
上边的`乱七八糟的` 唠嗑，好像跟`flutter` 并没有什么关系，不过
![20200315103454.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315103454.png)

在我们借用`Asd` 开启一个虚拟机设备调试的时候，可能会遇到一个问题，这就需要主机设备开启`虚拟` 一般情况下默认是不开启的。我是偏前端开发者，当然了看到这篇文章的你如果没在开发`app` 也不要走，因为技术就是金钱

## Koa2 初始化

**后端的服务选型** ，最初有几种方案

- node 原生开撸 （这个主要是写的太啰嗦）
- Express Node 的一个框架（早期的）这个也行
- Koa2 现在一般都更新到第二代了，V2.11.0
- eggjs 这个企业级约定俗称也还不错（在笔者的其他项目用了，这个 flutter 就不用了）
- Nestjs 这个同步接口文档十分方便（属于尝鲜玩法，也在笔者的其他项目用了，那就也先不用在这儿）

所以这个就先用大名鼎鼎的`Koa2` 先来说说我对 koa2 的理解

- 洋葱模型，兜一圈又回来
- 异步编程 可以说 koa2 很好实践 js 异步编程理念
- 可定制化，根据习惯随意开发，拓展性强

### 项目目录

```sh
├─app
│  └─api
│      └─v1  // RESTful API 接口规范 v1 版本
├─core    // 核心的代码
└─test
```

### 开发依赖

在前端的项目中，`package.json` 一般这个就是管理包文件的，那在我们的`flutter` 项目中使用`pubspec.yaml` 文件是一样的，差不多

```sh
"dependencies": {
    "koa": "^2.11.0", // 这个是项目依赖的koa 虽然名字还是koa但她已经是2代了
    "koa-router": "^8.0.8", // 这个是路由跳转的
    "require-directory": "^2.1.1"  // 这个等会再说
  }
```

当然了这只是项目的初始化，后续更新会在此基础上，所以还是强烈建议看一下的。也可以收藏，没事的时候翻出来看看

### 入口文件

目前还是用`js` 来开发，如果对`ts` 感兴趣也可以推门

- [春节间的 TypeScript 笔记整理](https://juejin.im/post/5e377a5de51d4530e60e4d1d)

```js
const Koa = require("koa");
const app = new Koa();
const Init = require("./core/init");
Init.entrance(app);
app.listen(3000);
```

在这里我们新建了一个`类` 主要就是初始化应用的，这一点在 `Nuxt` 和 `Next` 等等的框架中都有核心的体现，包括在`egg js` 中 ，

1. 导入 koa require("koa");
2. 实例化 new Koa();
3. 引入核心代码 require('./core/init')
4. 传入 app Init.entrance(app)
5. 监听端口 3000

还有一点十分重要就是在`node` 环境中模块化的规范不同于`es6` 的`import` 至于模块化规范，自行右转`google`

### 应用初始化类

```js
// 初始化加载路由
const requireDirectory = require("require-directory");
const Router = require("koa-router");
class Init {
  // 入口方法
  static entrance(app) {
    Init.app = app;
    Init.initRoute();
  }
  // 路由导入初始化
  static initRoute() {
    requireDirectory(module, "../app/api", { visit: visitor });

    function visitor(obj) {
      if (obj instanceof Router) {
        Init.app.use(obj.routes());
      }
    }
  }
}
module.exports = Init;
```

在这个文件中，我们引入了上文提及的`require-directory`

- 左转 [批量导入相关文件](https://www.npmjs.com/package/require-directory)

```JS
var requireDirectory = require('require-directory'),
  visitor = function(obj) {
    return obj(new Date());
  },
  hash = requireDirectory(module, {visit: visitor});
```

意识是说我们可以导入文件，那么我们要做的就是自动化注入路由文件

- user.js

  ```js
  // 个人中心v1-api
  const Router = require("koa-router");

  const router = new Router();

  router.get(`/api/v1/user`, (ctx, next) => {
    ctx.body = {
      code: 0
    };
  });
  module.exports = router;
  ```

我们整体遵循`RESTful API` 风格 api 不得不思考一个问题，关于后端接口迭代的问题，这也是为什么我们调用的接口会有`v1` `v2` 版本前缀，这对于规范化开发十分重要。所以我们把路由文件这样安排

```sh
 - app
 	- v1
 	  - home.js
 	- v2
 	- v3
 	……
```

### 启动后台服务

```sh
npm i // 没有几个包下起来很快
npm i -g nodemon // 自动监听文件变化，这在node开发过程中十分重要
```

```sh
nodemon app.js
```

直接在浏览器输入：

[本地 3000 端口，可尝试直接点击](http://localhost:3000/api/v1/user)

当看到接口返回的信息就说明后台的基本服务已经启动了，但是这还远远不够，远远的不够
![20200315121326.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315121326.png)

```json
{
  "code": 0,
  "data": {
    "nickName": "yayxs",
    "fav": [
      {
        "id": 1,
        "type": "writing"
      }
    ]
  },
  "msg": "获取用户信息成功"
}
```

- 一、这是我们自己的本地服务，当写了十分炫酷的服务，显然是不便分享到他人的
- 二、这也还是我们自己的写的测试的 json 数据，并没有连接数据库

顺便先说一下，这个项目咱们用`MySql` ,感兴趣的话，你也可以推门 [Node | 自我爬虫掘金专栏文章](https://juejin.im/post/5e532c53518825497312232f)

### 服务器部署

**核能预警**

一提到`服务器相关的知识`不要慌，我们一步步来实现`公网IP` 部署`node 服务`

#### 目标

> 目标一：掌握 pm2 部署 node JS 服务 进行守护，进程
>
> 目标二：掌握基本的 nginx 反向代理
>
> 目标三：暂时拜别本地服务

#### 效果

#### 云服务器准备

为什么说第一步要准备云服务器，因为哪怕你用`原生html` 或者说什什么的`ssr渲染框架` 或者说`jQ`

等等吧，哪怕是之前读书做的`告白网站`

![81OIpD.gif](https://s1.ax1x.com/2020/03/15/81OIpD.gif)

你总得放在公网上吧，不然总不能把女孩子拉到自己的家里，然后`npm run start`等等，你看你看………………

- 阿里云
- 腾讯云
- 华为云
- 国外的 vps 等等都差不多

可能国外的访问会受阻，所以还是国内的`BATH` 等等这几家的，都差不多真的不骗你

问：什么是云服务器?什么是域名解析？什么是部署？怎么反向代理？**那你能帮帮我吗？？**

答：你玩游戏的是啥 ，电脑，云服务器就是电脑（当然了在这里是不正确的也不是很准确的）

虽然我没有那么浪漫和骚，但是我有云服务器 还是包年的 **公网 IP http://62.234.111.140/**

希望大佬们不要对我做坏事情，跪拜

#### 连接远程服务器

![20200315123339.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315123339.png)

输入用户名密码连接就行了
![20200315123519.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315123519.png)
这样就可以了，我发现真的是**废话好多啊** 具体的细节，如果大家有什么疑问，可以再评论区留言，能力所及，会回复的。首先上来的时候要安装几个东西

```sh
npm i -g node  // 全局安装最新版的node环境
npm i -g pm2 // 全局安装线程管理
 // 等等等等
```


![20200315124004.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315124004.png)

一切的环境准备好之后，就需要同步一下咱们的服务端代码到`云服务器` 这一点同样十分的重要，不然就没得进行了。

#### 依赖三方服务器

总得有个同步的服务器，我们选择`github` 服务器，这样在云服务也好，还是咱们的本地电脑，代码最起码丢不了

我是放在了`home` 文件夹下
![20200315124901.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315124901.png)

那就装依赖呗，老套路

```
cd /home/flutter-koa2-du/koa2-server
npm i
```

趁着也安装一下`nodemon` 吧 答应我安装下好吗[npm-nodemon](https://www.npmjs.com/package/nodemon)

虽然说我们也是在本地开发然后同步到云服务器，云服务器的代码一般不会怎么变动，
![20200315125346.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315125346.png)

**启动项目**
![20200315125503.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315125503.png)

不要慌，解决问题

- 问题原因：主要是在同一环境3000这个端口已经被占用
- 解决问题：那就关闭3000 进程

这个时候我们就要引入`PM2` 纯纯的大写的高调的`pm2`

#### Pm2应用

首先来看下`pm2` 干些什么

- 内建负载均衡（使⽤Node cluster 集群模块、⼦进程，可以参考朴灵的《深⼊浅出node.js》⼀书 第九章） 
- 线程守护，keep alive
-  0秒停机重载，维护升级的时候不需要停机. 
- 现在 Linux (stable) & MacOSx (stable) & Windows (stable).
- 多平台⽀持 
- 停⽌不稳定的进程（避免⽆限循环）
-  控制台检测 https://id.keymetrics.io/api/oauth/login#/register 
- 提供 HTTP API

可能现在这样说，也没设好理解的，是有一个这样的场景，云服务器的环境可不像我们本地的电脑，即开发环境（dev），一旦上线，会有各种复杂的问题出现，导致程序崩掉。不能够为我们提供`服务`

##### 配置

```sh
npm install -g pm2
pm2 start app.js --watch -i 2
// watch 监听⽂件变化
// -i 启动多少个实例
pm2 stop all
pm2 list
pm2 start app.js -i max # 根据机器CPU核数，开启对应数⽬的进程
```

这只是简单的配置，详细的玩法可以自行右转`google` 也可以下翻参阅文章关于`pm2` 的分享，当然了还是要滑上来的

##### pm2 list

![20200315130743.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315130743.png)

我们可以通过`pm2 list` 查看进程启动情况，显然我们的项目已经在云服务器的`3000`端口启动了,那么这个时候我们把进程`stop all` 停掉

##### pm2 stop all
![20200315131034.png](https://raw.githubusercontent.com/yayxs/Pics/master/img/20200315131034.png)

我们通过命令先听到3000端口

#### pm2 优雅启动node进程服务

```sh
pm2 start app.js -i max -n node-koa-pm2
```

详细的含义自行`google` , ok 到这里应该就没什么问题了

#### curl 自行访问测试



## 其他

### 行文思路

- [vue-element-admin 是一个后台前端解决方案](https://panjiachen.github.io/vue-element-admin-site/zh/guide/)

### 参考阅读

- [node 服务开发和服务器部署](https://juejin.im/post/5e5a281be51d4526d059596d)
- [pm2---node 进程管理工具](https://juejin.im/post/5d26ffeaf265da1b9163bf15)
- 