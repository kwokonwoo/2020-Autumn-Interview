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