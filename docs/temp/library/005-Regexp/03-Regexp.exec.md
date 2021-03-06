# `Regexp.prototype.exec()`

## 描述

在一个指定字符串中执行一个搜索匹配。返回一个数组或 `null`。

## 参数

参数 | 描述
--- | ---
string | 必需。要匹配正则表达式的字符串。

## 返回值

如果匹配成功，`exec()` 方法返回一个数组，并更新正则表达式对象的属性。

返回的数组将完全匹配成功的文本作为第一项，将正则括号里匹配成功的作为数组元素填充到后面。

如果匹配失败，返回 `null`。

## 示例

```js
var str = 'leftTop';

var reg = /^([a-z]*)([A-Z]\w*)*/;

var result = reg.exec(str);

console.log( result );
```
打印结果：

![](http://p2btijoky.bkt.clouddn.com/18-3-15/94950726.jpg)


数组第一个元素：完全匹配成功的文本

数组第二个元素：匹配到正则第一个括号内表达式的文本

数组第三个元素：匹配到正则第二个括号内表达式的文本

（以此类推……）

数组的 `index` 属性：匹配成功的文本首个字符在原表达式中的索引

数组的 `input` 属性：用于匹配正则表达式的原始字符串
