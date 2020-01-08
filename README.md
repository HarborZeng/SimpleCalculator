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

# 一．项目结构
- 通体采用body内div相互嵌套的原则
- css使用外联，js内联
- 日历部分采用unordered list的list item通过向左float实现


# 二．文件资源命名规范
- class主要给css用，id主要给js用
- class和id的命名采用‘减号’将对象和功能隔离开

> 如：`calc-style.css		calc-header		calc-screen-container		calc-btn 
calc-number		calc-operator		calc-clear				calc-equal`

# 三．开发环境
- JetBrains WebStorm

# 四．编码规范
## 1.HTML编码规范
- HTML 文档头使用 HTML5 doctype 规范编辑
- 语法空格使用空格的形式，以保证在什么环境下打开都能有一致的阅读体验
- 不强制要求style标签和javascript标签的引用位置

## 2.CSS编码规范
- 命名要好看，见名知意
- 没有style代码写入HTML中
- css没有嵌套覆盖
- 模块和模块之间需要至少一行的空隙
- 颜色分明，背景颜色和`hover`颜色明显


## 3.JavaScript编码
- 使用事件绑定冒泡的方式来实现对list item的点击事件
- 定义全局变量`formula`存储用户点击的按钮代表的算式
- 定义全局变量`result`存储计算结果，实时将显示到`calcScreen`（计算器屏幕）上面
- 给`ul`标签绑定匿名点击事件，通过`event.target.innerHTML`来获知用户点击的具体是哪一个按钮，针对具体事件，对`formula`执行操作
- 点击数字和加减乘除小数点，就简单的`+`之
- 点击`clear`执行`formula`和`calcScreen`清空操作
- 点击`delete`执行`formula`取`substr`和`calcScreen`重新显示`formula`操作
- 点击`=`，使用`eval`函数，将现有`formula`进行运算，值赋给`result`，回显到`calcScreen`，出错回显“式子错误”
- 点击`pow`和`sqrt`，`+`上相应的`Math`代码

# 四．项目部署
<http://tellyouwhat.cn/SimpleCalculator/Calculator.html>

