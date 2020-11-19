### No silver bullet
#### HTML
- cookie、session、sessionStorage、localStorage
- 行内元素和块级元素
#### CSS
- 盒子模型
- BFC
- 继承性
- **选择器优先级**
  - 类型选择器（h1）和伪元素（::before）< 类选择器（.example），属性选择器（[type=”radio”]）和伪类（:hover）< ID选择器（#example）
  - 通配选择符、关系选择符和否定伪类对优先级没有影响。
  - 元素的内联样式总会覆盖外部样式表的任何样式，可看作具有最高的优先级。
  - !important声明会覆盖其他任何声明，应该避免使用!important，因为其破坏了样式表中的固有的级联规则，增加了调试的难度。
- 伪类和伪元素
  - 伪类是选择器的一种，类似向文档某部分添加了一个类，比如选中某个类型的第一个元素，或者当鼠标指针悬浮在元素上面时。（\<article>下的第一个段落或\<ul>下的第一个\<li>）
  - 伪元素类似向文档中加入全新的HTML元素。（选中段落中的第一行文字）
- **垂直居中**
- 两列布局
- 三列布局
- 隐藏页面元素
- 移动端适配
- 响应式布局
- CSS 3新特性
  - 动画
  - flex box

#### JavaScript
- this
- 闭包
- 0.1+0.2问题
  - `numberObj.toFixed(digits)`
  ```js
  +(0.1 + 0.2).toFixed(1);
  ```
  - `numberObj.toPrecision(precision)`
  ```js
  function strip(number) {
    return (parseFloat(number.toPrecision(12)));
  }
  strip(0.1 + 0.2);
  ```
  ```js
  function isEqual(a, b) {
    return Math.abs(a - b) < Number.EPSILON;
  }
  isEqual(0.1 + 0.2, 0.3);
  ```
- 类型判断
- **原型和继承**
- 深拷贝
- 隐式转换
- DOM常用操作
- 函数的call、apply和bind
- Ajax
- 发布订阅模式
- 构造函数new
  - 过程
  - 实现
- 事件循环
  - 宏任务与微任务
- 防抖和节流
- 函数式编程
- 函数柯里化
- 设计模式
  - 工厂模式
- **ES6**
  - **let和const**
  - **箭头函数**
  - **Promise**
  - 循环语法
  - async、await
  - Class静态方法和公共方法

#### Vue
  - v-if和v-show
  - 组件通信
  - **Vuex**
  - 双向绑定原理
  - MVVM模式
  - 生命周期
  - Computed和watch的区别
  - key

#### HTTP
  - HTTP请求头
  - **常见的状态码**
  - TCP三次握手和四次挥手
  - GET和POST的区别
  - HTTP1.0和2.0的区别
  - HTTP和HTTPS的区别
  - TCP和UDP的区别

#### Algorithm
  - 常见的排序算法
  - 二分查找
  - **数组去重**
  - 数组乱序
  - 数组各种方法实现
    - flat
    ```js
    function flatten(source, target = []) {
      for (const item of source) {
        if (Array.isArray(item)) {
          flatten(item, target);
        } else {
          target.push(item);
        }
      }
      return target;
    }
    ```
    - reduce
    ```js
    function flatten(source, target = []) {
      for (const item of source) {
        if (Array.isArray(item)) {
          flatten(item, target);
        } else {
          target.push(item);
        }
      }
      return target;
    }
    ```
    - map
    - filter
    - find

 
#### Web
  - 从输入URL到浏览器完成页面渲染都发生了什么
  - 跨域
  - 浏览器的缓存机制
  - **回流（重排）与重绘**
  - 性能优化
    - 懒加载
  - 安全
    - XSS
    - CSRF

#### Computer fundamental
  - 线程与进程
  - 常见的git命令
