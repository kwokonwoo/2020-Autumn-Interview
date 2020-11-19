# token
# cookie
HTTP Cookie是服务器发送到用户浏览器并保存在本地的一小块数据，它会在浏览器下次向**同一服务器**再发起请求时被携带并发送到服务器上，从而可以实现一下的目的：
- 保持用户登陆状态
- 自定义设置、主题等
- 跟踪分析用户行为

服务器在响应HTTP请求时，通过发送Set-Cookie HTTP头部包含会话信息：
```js
HTTP/1.1 200 OK
Content-type: text/html
Set-Cookie: name=value
```
浏览器会存储这些会话信息，并在之后的每个请求中通过HTTP头部cookie将它们发回服务器：
```js
GET /sample_page.html HTTP/1.1
Host: www.example.org
Cookie: name=value
```
打开开发者工具可以看到cookie由以下部分构成：
- 名称（name）：唯一标识的名称。如此页面的“dotcom_user”。
- 值（value）：存储在cookie里的字符串值。如此页面的“kwokonwoo”。
- 域（domain）：cookie有效的域。
- 路径（path）：请求URL中包含这个路径才会把cookie发送到服务器。
- 过期时间（expires）：表示何时删除cookie的时间戳。
- 安全标志（secure）：设置之后，只在使用SSL安全连接的情况下才会把cookie发送到服务器。

JavaScript可以通过`document.cookie`创建新的cookie，也可通过该属性访问非HttpOnly标记的cookie。
```js
document.cookie = "yummy_cookie=choco";
document.cookie="tasty_cookie=strawberry";
console.log(document.cookie);

// "yummy_cookie=choco; tasty_cookie=strawberry"
```

# session

# Web Storage
localStorage是永久存储机制，sessionStorage是跨会话的存储机制。
大多数浏览器给localStorage和sessionStorage设置了每个源（协议、域和端口）5MB的空间限制。

## sessionStorage
sessionStorage对象只存储会话数据，数据只会存储到浏览器关闭。存储在sessionStorage中的数据不受页面刷新影响，可以在浏览器奔溃并重启后恢复。

## localStorage
localStorage作为在客户端持久存储数据的机制，要访问同一个localStorage对象，页面必须来自同一个域（子域不可以）、在相同的端口上使用相同的协议。

localStorage中的数据会保留到通过JavaScript删除或用户清楚浏览器缓存。localStorage数据不受页面刷新影响，也不会因关闭窗口、标签页或重启浏览器而丢失。

## Reference
https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Cookies

https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/Client-side_web_APIs/Client-side_storage

马特·弗里斯比. JavaScript高级程序设计：第4版，P751-771.
