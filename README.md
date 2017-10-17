# SimpleCalculator
基于html、css和javascript的一个简单计算器

# 设计方法：
- html
使用`div`和`ul`标签布局

- css
使用`calc-*`class来定义标签的样式

- javascript
在`li`标签中，使用`onclick`属性绑定事件`inputSign(sign)`，`deleteLastStr()`，`evaluateInput()`和`clearAll()`
计算使用`eval()`函数，将`formula`表达式进行求值
