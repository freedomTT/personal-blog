---
title: JavaScript知识点记录
date: 2020-05-03 14:36:34
categories:
- 学习笔记
tags: 
- js
---

记录一些平时遇到的问题；

1、什么是引用传递？

js有引用传递和值传递，字符串、number是值传递。对象作为函数的参数传递进去，是引用传递，但是，在函数只能对对象参数进行原有方法操作，比如splice，不能进行赋值操作，复制操作将改变引用地址。

2、什么是发布订阅？

观察者模式和订阅模式，观察者模式有两个主要对象，Subject 和 Observer ，Subject 实现保存，删除，通知的方法。Observer 中存储事件 。订阅模式比观察者模式多了一个中间代理。

3、querySelect方法跟getELementById有什么区别？

H5新增方法，ie6 7不支持。用法 document.querySelect('#id')

4、createDocumentFragment是什么方法？

用于虚拟dom

5、call apply 执行函数方法，this指向？

三个方法的作用都是改变函数内部的this指向并且传递参数。 使用方法：
```
fun.call(obj,param1,param2);
fun.apply(obj,[param1,param2]);
fun.bind(obj,param1,param2); // 返回的是方法。需要()来执行。
```
6、RegExp相关知识 $1 、()是什么东西？

()在正则表达式中分组，用$1,$2, $3 ...访问

<!-- more -->

7、了解flow。

类似typescript，给js加上类型 方便维护 。

8、chinaWebpack相关。

链式修改、添加loader

9、webpack中require.context相关。

在webpack中用来引入文件夹下的多个文件。require的context方法生成一个 context module(上下文模块)，它包含目录下的所有模块的引用，是通过一个 request 解析出来的正则表达式，去匹配目录下所有符合的模块，然后都 require 进来。此 context module 包含一个 map 对象，会把 request 中所有模块翻译成对应的模块 id。

require.context(path,isRecursive,reg)
10、vue directive

例如 v-model 之类的；可以自定义；参数 el,binding:{name,value,oldValue,expression,arg,modifiers},vnode,oldNode

11、学习typescript

12、while循环

while(条件语句){
    执行代码
}
do{
    执行代码
}while(条件语句)
13、CommonJs、AMD、CMD、ES6模块

commonJS 应用于nodejs AMD 异步模块定义，require.js CMD SeaJs es6模块 export import

14、require.resolve

输出带有文件名的完整路径 等效

path.join(__dirname, './assets/some-file.txt')
//等效
require.resolve('./assets/some-file.txt')
15、es6 数组的 some every方法

遍历数组 判断是否满足条件。 some 一真即真 every 所有真才为真 example:

const arr = [1,2,3]
const result = arr.some(item => item > 2)
//result 等于 true
17、hooks 是什么

18、Electron 是什么

19、PWA 相关
