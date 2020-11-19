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