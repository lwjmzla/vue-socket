# Vue.js+Socket.io+express打造一个智能聊天室

## 技术栈
* **Vue2.0**：前端页面展示。
* **Socket.io**：实现实时通信
* **Vuex**：Vuex，实现不同组件间的状态共享
* **vue-router**：页面路由切换
* **axios**：一个基于 `Promise` 的 HTTP 库，向后端发起请求。
* **Express**、**Koa2**：因为vue-cli生成的项目是基于**express**的，所以在开发阶段我使用的是它，但是真正上线生产环境我换成了**Koa2**。
* **Moment.js**：一个时间处理的库，方便对时间进行格式化成需要的格式。
* **ES6**、**ES7**：采用ES6语法，这是以后的趋势。箭头函数、Promise等等语法很好用。
* **localStorage**：保存用户信息以及聊天记录。
* **Webpack**：vue-cli自带Webpack，但是需要自己改造一下，比如要对需要安装sass相关loader，vue-cli已经配置好了webpack，你只需要安装依赖就可以，使用的时候只需要`<style lang="scss"></style>`。
* **SASS**(**SCSS**)：用SCSS做CSS预处理语言，有些地方很方便，个人很喜欢用。(详看👉[SASS用法指南](https://microzz.com/2017/03/18/sass/))
* **flex**：flex弹性布局，**简单**适配手机、PC端。
* **CSS3**：CSS3过渡动画及样式。

