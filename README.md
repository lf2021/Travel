# Travel

### 这是一个 vue 框架搭建的一个简易的旅游网站，模拟去哪儿网移动端的设计，下面列举了使用的相关的技术栈：

1. Webpack--打包工具
2. Bootstrap--前端开发的开源工具包
3. Swiper--移动端网页触摸内容滑动 js 插件
4. better-scroll--解决移动端各种滚动需求的插件
5. Ajax--获取服务器端数据
6. Stylus--CSS 预处理框架
7. Axios--基于 promise 的 HTTP 库
8. Json--存储数据的格式
9. Vuex--vue.js 的中心化状态管理方案

# 1.安装 node.js (运行在服务器端的 JavaScript)

官网下载 LTS 版本(长期维护的版本)

通过命令行

```
node -v
```

查看一下版本号判断一下 node 是否安装成功

通过命令行

```
npm -v
```

查看一下 node 是否也成功安装

# 2.在 Gitee 或者 GitHub 上创建仓库

初始化仓库...

# 3.安装 git

在命令行通过

```
git --version
```

看一下 git 是否安装成功

# 4.公钥认证

通过终端 git bash 运行 Linux 命令

你可以按如下命令来生成 sshkey:

```
ssh-keygen -t rsa -C "xxxxx@xxxxx.com"

# Generating public/private rsa key pair...
# 三次回车即可生成 ssh key
```

查看你的 public key，并把他添加到码云（Gitee.com）

```
cat ~/.ssh/id_rsa.pub
# ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC6eNtGpNGwstc....
```

添加后，在终端（Terminal）中输入

```
ssh -T git@gitee.com
```

若返回

```
Welcome to Gitee.com, yourname!
```

则证明添加成功。

# 5.项目克隆到本地

### 本地初始化一个项目

首先，你需要执行下面两条命令，作为 git 的基础配置，作用是告诉 git 你是谁，你输入的信息将出现在你创建的提交中。

```
git config --global user.name "你的名字或昵称"
git config --global user.email "你的邮箱"
```

然后在你的需要初始化版本库的文件夹中执行：

```
git init
git remote add origin <你的项目地址> //注:项目地址形式为:https://gitee.com/xxx/xxx.git或者 git@gitee.com:xxx/xxx.git
```

这样就完成了一次版本你的初始化。

如果你想克隆一个项目，只需要执行：

```
git clone <项目地址>
```

### 完成第一次提交

进入你已经初始化好的或者克隆项目的目录,然后执行：

```
git pull origin master
<这里需要修改/添加文件，否则与原文件相比就没有变动>
git add .
git commit -m "第一次提交"
git push origin master
```

然后如果需要账号密码的话就输入账号密码，这样就完成了一次提交。

此时，你可以在你的个人面板、项目主页查看到你的提交记录

按照本文档新建的项目时，在码云平台仓库上已经存在 readme 文件，故在提交时可能会存在冲突，这时您需要选择的是保留线上的文件或者舍弃线上的文件，如果您舍弃线上的文件，则在推送时选择强制推送，强制推送需要执行下面的命令：

```
git push origin master -f
```

如果您选择保留线上的 readme 文件,则需要先执行：

```
git pull origin master
```

然后才可以推送。

# 6.vue 初始化

全局安装 vue-cli

```
npm install --global vue-cli
```

创建一个基于 webpack 模板的新项目(webpack 是前端最流行的打包编译工具)

```
vue init webpack my-project
// my-project是你的项目根目录
```

进入项目目录下

```
cd (D:/Travel)
// ()里是项目路径
```

运行

```
npm run dev
```

# 7.项目代码结构介绍

> package.json
>
> 是存放的开发过程中存放的一些依赖

> package-lock.json
>
> 是 package 的一个锁文件，确定安装的一些第三方包的版本

> index.html
>
> 是默认的首页模板文件

> .postcssrc.js
>
> 是对 postcss 的一个配置项

> .gitignore
>
> 是在上传代码的时候，有一些特殊的文件不希望上传就在这个里面配置
> .eslintrc.js
>
> 配置了代码的规范

> .eslintignore
>
> 哪些文件不会受 eslint 规范，配置在此文件里

> .editorconfig
>
> 配置了编辑器里的语法

> .babelrc
>
> 我们的项目是 vue 的单文件组件的代码写法，需要通过 babel 这种语法解析器做一些语法上的转换，最终转换成浏览器能够编译执行的代码

> static 文件
>
> 里面存放的是一些静态的资源（静态的图片啊，JSON 数据等）

> node_modules 文件
>
> 我们这个项目所依赖的一些第三方的包

> src 文件
>
> 存放的是我们整个项目的代码：
>
> > main.js
> >
> > 是整个项目的入口文件
>
> > App.vue
> >
> > 是项目最原始的根组件
>
> > router 文件
> >
> > 存放项目所有的路由
>
> > components 文件
> >
> > 存放的是项目里的小组件
>
> > assert 文件
> >
> > 存放我们项目里用到的一些图片类的资源

> config 文件
> 放的是一些项目的配置文件
>
> > index.js
> >
> > 放基础的配置文件
>
> > dev.env.js
> >
> > 放开发环境的一些配置信息
>
> > prod.env.js
> >
> > 放线上环境的一些配置信息

> build 文件
> 放的是项目打包的 webpack 的一些配置内容，是 vue-cli 自动帮我们配置好的 webpack 配置的集合，一般来说不需要去修改
>
> > webpack.base.conf.js
> >
> > 配置基础的 webpack 配置项
>
> > webpack.dev.conf.js
> >
> > 开发环境的 webpack 配置项
>
> > webpack.prod.conf.js
> >
> > 线上环境的 webpack 配置项

# 8.需要的一些文件

下面的文件都放在 src/assets/styles/目录下,并且需要在项目的入口文件 main.js 中导入

(1) 需要一个 reset.css 来统一手机浏览器样式

(2) 需要一个 border.css 来解决移动端 1 像素边框的问题

(3) 移动端 300ms 点击延迟，通过导入一个 fastclick 库来解决，通过下面命令将 fastclick 安装在项目的依赖中，可在 package.json 中的 dependencies 中查看到

```
npm install fastclick --save
```

(4) iconfont 来保存一些图标字体

# 9.安装一些方便的依赖

stylus

```
npm install stylus --save
```

stylus-loader

```
npm install stylus-loader --save
```

vue-awesome-swiper 轮播插件(为确保项目正常，选择 2.6.7 版本)

```
vue install vue-awesome-swiper@2.6.7 --save
```

> 因为我们在整个项目都可能用到轮播，所以我们在全局引入这个轮播插件，在 main.js 中引入
>
> > import Vue from 'vue'
> >
> > import VueAwesomeSwiper from 'vue-awesome-swiper'
>
> 还需引入 css 文件
>
> > import 'swiper/dist/css/swiper.css'
>
> 使用方式
>
> > Vue.use(VueAwesomeSwiper)

# 10.简易操作

将一些通用的样式放在一个文件里

在./src/assets/styles/建立一个 variables.styl 文件，在其中保存一些公共的样式，例如：

```
$bgColor = #00bcd4
$darkTextColor = #333
$headerHeight = .86rem
```

src 目录可以简写成'@'，但是在 css 中想引入 src 目录下的文件要用'~@'，即需要加一个小波浪线

在 webpack.base.conf.js 中 resolve 中的 alias 里可以配置，例如：

```js
'@': resolve('src'),
'styles': resolve('src/assets/styles'),
'common': resolve('src/common'),
```

# 11.通过分支来添加内容，确保没问题再合并到 master

先在线上创建一个分支

然后在终端输入

```
git pull
```

可以获得分支信息，通过

```
git checkout branchName
```

来切换分支

# 遗留问题：

在最后解决 detail 文件下 Detail.vue 不同的 banner 触发 ajax 请求问题上，视频教学上是选择在 App.vue 根组件上的 keep-alive 标签上做出了改变：

#### &#60;keep-alive exclude="Detail"&#62;

#### &#60;router-view/&#62;

#### &#60;/keep-alive&#62;

但是会存在一个问题，detail 组件下的 Header.vue 的渐隐渐现效果直接没了。
