---
layout: default
title:  Menu组件
parent: UI组件
nav_order: 1
---

# Menu组件

项目内嵌了一个针对`element-ui`纵向菜单组件的封装。可以针对传入的数据自动区分使用`<el-submenu />` 和 `<el-menu-item />`

组件在 `src/views/home/components/Menu.vue`中

## 使用

```js
// 引入
import Menu from './components/Menu'
// 在项目中注册
components: { Menu }

// 使用
 <Menu :menuData="menuData" />
``

## 参数说明

只接受一个参数 `menuData`。

menuData示例：

```js
const menuData: [
    {
        title: '导航一',
        icon: 'el-icon-notebook-2',
        children: [ //如果有
            {
                title: '选项1',
                children: [
                    {
                        title: '关于',
                        link: './about',
                    },
                ],
            },
        ],
    },
    {
        title: '导航二',
        icon: 'el-icon-suitcase',
        children: [
            {
                title: '选项1',
                icon: 'el-icon-tickets',
                link: '',
            },
        ],
    },
    {
        title: '导航三',
        icon: 'el-icon-tickets',
        disabled: true,
    }
]
```
属性说明：

|属性名| 功能 |
|:---|:---|
| title | 标题 |
| icon | 栏目对应的图表（使用element-u自带的）|
| disabled | 如果有并且是true，则不能使用 |
| link | 跳转地址 |
| children | 如果有，则表示还有下一层级；如果没有下一层级，建议不用使用children |