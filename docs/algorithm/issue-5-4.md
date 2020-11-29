https://www.ecma-international.org/ecma-262/6.0/#sec-array.prototype.slice
```js
Array.prototype.mySlice = function(start, end) {
  let len = this.length;
  let l = start === undefined ? 0 : start < 0 ? Math.max(start + len, 0) : Math.min(start, len);
  let r = end === undefined ? len : end < 0 ? Math.max(end + len, 0) : Math.min(end, len);
  const res = [];
  while (l < r) {
    res.push(this[l++]);
  }
  return res;
}
```
