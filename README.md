# vue-nice-loading

一个大概会好用的`loading`

安装
```javascript
npm i vue-nice-loading
```
在`main.js`中引入
```javascript
import loading from 'vue-nice-loading'

Vue.use(loading)
```
使用`Vue.use`初始化后会在`vue`原型上注册`$loading`，调用`$loading`方法显示`loading`，并返回实例，调用实例的`close`方法可以关闭该`loading`
```javascript
// 显示loading
let loading = this.$loading({
  text: 'loading'
})
// 关闭loading
setTimeout(() => {
  loading.close();
}, 3000)
```
`$loading`方法接受以下参数

**type**

`loading`显示的种类，这里使用的所有`svg`图片取自['SVG-Loaders'](https://github.com/SamHerbert/SVG-Loaders), 接受值与图片名相同，默认值为`three-dots`，共有以下12种
- audio
- ball-triangle
- bars
- circles
- grid
- hearts
- oval
- puff
- rings
- spinning-circles
- tail-spin
- three-dots

**target** 

`loading`需要覆盖的`dom`节点, 可传入一个`dom`对象或选择器的字符串，默认为`body`，显示全屏`loading`
```javascript
this.$loading({
  target: '#app'
  // target: this.$refs.app
  // target: document.querySelector('#app')
})
```
**text**

显示文本，默认为空

**background**

遮罩层背景色

**delay**

延时显示，单位为毫秒，以下例子会在1s后显示
```javascript
this.$loading({
  delay: 1000
})
```