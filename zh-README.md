<h1 align="center">vuepress-plugin-right-anchor</h1>
<div align="center">

![Version](https://img.shields.io/github/package-json/v/xuekai-china/vuepress-plugin-right-anchor?style=flat-square)
![NPM](https://img.shields.io/npm/l/vuepress-plugin-right-anchor?style=flat-square)

</div>

[English](./README.md) ｜中文

> 在用 VuePress 编写的文档页面右侧添加 **锚点导航栏**

## 特性
  - 简化左侧边栏结构的同时不丢失页面内标题导航的功能。
  - 点击锚点标签页面滚动过度。
  - 页面滚动时对应锚点标签跟随高亮。

## 示例
  [soonspacejs 文档](http://www.xwbuilders.com:9018/soonspacejs/Docs/api/sbm.html)

## 安装
```bash
yarn add vuepress-plugin-right-anchor -D
# or
npm i vuepress-plugin-right-anchor -D
```

## 使用
在 `.vuepress/config.js` 添加如下配置。 
```js
module.exports = {
  // ...
  plugins: [
    // ...
    ['vuepress-plugin-right-anchor']
  ]
}
```

## 配置
在 `.vuepress/config.js` 添加如下配置。 
```js
module.exports = {
  // ...
  plugins: [
    // ...
    [
      'vuepress-plugin-right-anchor',
      {
        showLevel: 1,
        ignore: [
          '/',
          '/api/'
          // 更多...
        ]
      }
    ]
  ]
}
```

## 参数说明

### showLevel

  在右锚显示中将使用哪一级别的标题。
  该值的指向含义与 [themeconfig.sidebardept](https://vuepress.vuejs.org/zh/theme/default-theme-config.html#%E4%BE%A7%E8%BE%B9%E6%A0%8F) 相同。

  - Type: number
  - Default: 1

### ignore

  不显示 right-anchor 的页面。

  - Type: array
  - Default: []