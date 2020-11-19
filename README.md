### No silver bullet
#### HTML
- [cookie、session、sessionStorage、localStorage](docs/html/issue-1.md)
- [行内元素和块级元素](docs/html/issue-2.md)
#### CSS
- [盒子模型](docs/css/issue-1.md)
- [BFC](docs/css/issue-2.md)
- [继承性](docs/css/issue-3.md)
- [**选择器优先级**](docs/css/issue-4.md)
- [伪类和伪元素](docs/css/issue-5.md)
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
