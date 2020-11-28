基本的语法形式：
```css
@media media-type and (media-feature-rule) {
  /* CSS rules */
}
```

当视口宽度窄于600px时，body当文本变成红色：
```css
@media screen and (max-width: 600px) {
  body {
    color: red;
  }
}
```
