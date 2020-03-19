# travel
  ### 这是一个vue框架搭建的一个简易的旅游网站，模拟去哪儿网移动端的设计，下面列举了使用的相关的技术、工具、插件：
  1. Webpack--打包工具
  2. Bootstrap--前端开发的开源工具包
  3. Swiper--移动端网页触摸内容滑动js插件
  4. better-scroll--解决移动端各种滚动需求的插件
  5. Ajax--获取服务器端数据
  6. Stylus--CSS预处理框架
  7. Axios--基于promise的HTTP库
  8. Json--存储数据的格式
  9. Vuex--vue.js的中心化状态管理方案
   
# 遗留问题：
在最后解决detail文件下Detail.vue不同的banner触发ajax请求问题上，视频教学上是选择在App.vue根组件上的keep-alive标签上做出了改变：

<keep-alive exclude="Detail">
  <router-view/>
</keep-alive>

但是会存在一个问题，detail组件下的Header.vue的渐隐渐现效果直接没了。