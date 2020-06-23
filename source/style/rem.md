---
title:  rem功能
---

# rem功能

文件配置在`src/assets/rem.scss`中。

根据我们平时的设计规范，默认是宽度750px的设计稿。文件内部通过修改`$device-width`可以改变基准宽度。

## 像素转rem

引入rem文件

```scss
@import '@/assets/rem.scss';
```
使用

```scss
// 假设要把100px转换成rem单位的
@include rem(100) 
```