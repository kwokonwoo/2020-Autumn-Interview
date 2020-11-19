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

# Web Storage

## Reference
https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Cookies

马特·弗里斯比. JavaScript高级程序设计：第4版，P751-771.
