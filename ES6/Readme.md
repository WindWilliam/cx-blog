# 🐼 ES6标准

> 阮一峰ES6 标准入门一书 部分感觉对自己有帮助的内容摘录

## 1.介紹
### 1.1 ECAMScript 和 JavaScript的关系
> 讲清这个问题，需要回顾1996年11月，**JavaScript**创建者--**Netscape**(网景)公司，希望**JavaScript**能够成为国际标准，于是把**JavaScript**交给了ECMA(国际化标准组织)。次年ECMA发布262号标准文件(ECMA-262)的第一版,规定了浏览器脚本语言标准，并将这种语言称之为ECMAScript，这就吃第一版

### 1.2 ES6和ECMAScript2015的关系
> 2011年，ECMAScript 5.1版本发布后,6.0版本便开始制定。因此，ES6原意是指**JavaScript**的下一个版本

>由于经常会有新的语法提案，标准评委会每个月都会开会发步新标准。最后标准评委会决定每年6月份发布一次标准，版本号直接用年份标记即可。

### 1.3 babel-polyfill
> Babel默认值转换新的JavaScript句法,而不转行新的api，如Iterator,Set,Promise,Sumbol等,以及一些定义在全局对象上的方法（如Object.assign）都不会转码。

> 必须使用[**`babel-polyfill 点击查看详情`**](https://babeljs.io/docs/usage/polyfill/)提供一个垫片环境

## 2.[🎨 let and const](./section1/Readme.md)

## 3.[☝ 变量的解构赋值](./section2/Readme.md)

## 4.[👷 字符串的拓展](./section3/Readme.md)

## 5.[® 正则的拓展](./section4/Readme.md)

## 6.[® 数值的拓展](./section5/Readme.md)

## 7.[⚱ 函数的拓展](./section6/Readme.md)