- get和post请求的区别
  - get获取数据（幂等），post上传数据（非幂等）
  - get在浏览器中有长度限制
  - 本质上都是明文传输，都不安全（get可以被缓存，参数存储在浏览历史中，参数显示在URL中）
- 状态码
   - 304： not modified，表示资源在由请求头中If-Modified-Since（If-None-Match）参数指定的这一版本后，未曾被修改。
- 数组扁平化
```js
function flatten(source, target = []) {
  for (const element of source) {
    if (Array.isArray(element)) {
      flatten(element, target); // 一定要带上第二个参数
    } else {
      target.push(element);
    }
  }
  return target;
}
```
- v-for循环中的key
  - 如果不使用key，Vue会尽可能尝试就地修改/复用相同类型元素
- ES5/ES6的继承
  - class声明类似于let和const声明，存在暂时性死区
  - class声明内部会启用严格模式
  - class的所有方法都不可枚举（无法通过Object.keys取到）
  - class的所有方法都没有prototype，不能通过new调用
  - 必须使用new调用class
- HTTP 1/2
  - 在HTTP/1.1中，浏览器在同一时间针对同一域名下的请求有数量限制。超过数目会被阻塞。
  - HTTP2主要是通过启用完整的请求和响应多路复用来减少延迟。允许通过单一的HTTP/2连接发起多重的请求/响应消息。
    - 实现的关键在HTTP/2和传输层（TCP/UDP）之间增加一个二进制分帧层。
- 计数器
```
let count = (function() {
  let counter = 0;
  return function() {
    return (++counter)
  }
})()
```
