  - 类型选择器（`h1`）和伪元素（`::before`）< 类选择器（`.example`），属性选择器（`[type=”radio”]`）和伪类（`:hover`）< ID选择器（`#example`）
  - 通配选择符、关系选择符和否定伪类对优先级没有影响。
  - 元素的内联样式总会覆盖外部样式表的任何样式，可看作具有最高的优先级。
  - `!important`声明会覆盖其他任何声明，应该避免使用`!important`，因为其破坏了样式表中的固有的级联规则，增加了调试的难度。
