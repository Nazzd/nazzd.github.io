---
title: Prettier配置
date: 2024-03-12T14:14:22+08:00
author: Nazzd
tags: [Prettier]
categories: [Prettier]

---

## Prettier

#### 测试地址： [Prettier](https://prettier.io/playground/)

#### 部分配置：

- `trailingComma` ：对象的最后一个属性末尾也会添加 `,` ，比如 `{ a: 1, b: 2 }` 会格式为 `{ a: 1, b: 2, }` 
- `tabWidth` ：缩进大小
- `semi` ：是否添加分号
- `singleQuote` ：是否单引号
- `jsxSingleQuote` ：jsx 语法下是否单引号。
- `endOfLine` ：与 `.editorconfig` 保持一致设置
- `printWidth` ：单行代码最长字符长度，超过之后会自动格式化换行
- `bracketSpacing` ：在对象中的括号之间打印空格， `{a: 5}` 格式化为 `{ a: 5 }` 
- `arrowParens` ：箭头函数的参数无论有几个，都要括号包裹。比如 `(a) => {}` ，如果设为 `avoid` ，会自动格式化为 `a => {}` 

#### 安装配置流程

1. 安装prettier插件和vscode扩展 [Prettier - Code formatter](https://link.juejin.cn/?target=https%3A%2F%2Fmarketplace.visualstudio.com%2Fitems%3FitemName%3Desbenp.prettier-vscode "https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode") ：

2. 在项目根目录新建一个文件夹 `.vscode` ，在此文件下再建一个 `settings.json` 文件

代码保存时会自动格式化代码

```json
{
  // 保存自动格式化代码
  "editor.formatOnSave": true,
  // 开启stylelint自动修复
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

3. prettier配置

```js
module.exports = {
  // 每行最大列，超过换行
  printWidth: 120,
  // 使用制表符而不是空格缩进
  useTabs: false,
  // 缩进
  tabWidth: 2,
  // 结尾不用分号
  semi: false,
  // 使用单引号
  singleQuote: true,
  // 在JSX中使用单引号而不是双引号
  jsxSingleQuote: true,
  // 箭头函数里面，如果是一个参数的时候，去掉括号
  arrowParens: 'avoid',
  // 对象、数组括号与文字间添加空格
  bracketSpacing: true,
  // 尾随逗号
  trailingComma: 'none',
}
```
