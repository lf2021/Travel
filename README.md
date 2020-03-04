# travel

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

遗留问题：
在最后解决detail文件下Detail.vue不同的banner触发ajax请求问题上，视频教学上是选择在App.vue根组件上的keep-alive标签上做出了改变：

<keep-alive exclude="Detail">
  <router-view/>
</keep-alive>

但是会存在一个问题，detail组件下的Header.vue的渐隐渐现效果直接没了。