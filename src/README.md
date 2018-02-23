## 创建过程

1. github 创建仓库 ==> name + description + Add .gitignore + node

2. ` git clone ` ==> 复制到本地

3. ` npm init ` ==> 初始化

4. ` npm i -g vue-cli ` ==> 全局安装 vue-cli

5. ` vue init webpack . ` ==> vue 初始化

6. ` npm install ` ==> 安装依赖

7. ` npm run dev ` ==> 运行


## 引入第三方 css
```
npm i -S normalize.css
```
main.js ==> ` import 'normalize.css' `

## normalize.css 与 reset.css
normalize.css ==> 别人写的 ==> 让页面默认的样式在每一个浏览器中都是一样的，从而达到同意默认样式的目的
reset.css ==> 自己写的 ==> 个性化设置，即自定义样式

正确使用方式：先 normalize.css 再 reset.css


## scss 相关
```
npm i -D 找不到的模块
npm i -D sass-loader
```
#### 组件中使用 scss
` <style lang="scss"></style> `



## 注册全局组件

1. main.js ==> ` Vue.component() ` ==> ` new Vue() ` 初始化实例之前

2. main.js ==> ` import Hello from './components/Hello' ` + ` Vue.component('Hello', Hello) ` 