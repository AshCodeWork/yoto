---
layout: default
title:  request请求
nav_order: 3
has_children: true
---
# request请求

项目中使用axios作为请求工具。虽然包装了axios，但没把get请求和post请求改成一致的，原因是想让开发知道实际上这两种请求方式在axios中写法是有区别的。

请求工具满足以下功能。

* get请求
* post请求
* body请求
* 纯请求，不带额外参数

在项目中的demo页面中例子，例子中使用mock.js模拟了实际中的请求。mock的配置在`public/mock/index.js`中
{: .label .label-yellow }