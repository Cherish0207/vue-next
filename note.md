## 初始化项目

```bash
git clone git@github.com:vuejs/vue-next.git --depth 1
rm -rf .git
git init
```

## 源码使用方式

1. 安装依赖

- 因为源码里用的是 `menorepo` 的规则，所以只能`yarn install`，不能`npm install`

2. 使用

- `npm run dev`默认找的是`packages/vue`包，并不是把所有包的方法都暴露在了全局下，当
- `yarn run build`把所有包都打包

3. 看源码的几种方案

- 从单元测试入手,可以看一些特殊场景

## 查看 `package.json`

- `npm run dev`:开发可以方便调试实时监控源码的变化
- `npm run build`把`packages`:所有的包都进行打包

## `menorepo`

> 一个项目下管理多个包
> 如`element-plus`,把每个组件都抽成一个包,我们可以单独使用某个包,而且可以方便知道某个组件的下载量

## 副作用函数 effect

> vue 模块是所有包的整合，但并不导出所有包的 `api` 方法，如 `effect`

- 后续会基于 `effect`实现`watch effect`、`watch api`、计算属性等很多功能，是响应式的核心
- `vue3-effect` & `react-effect` & `vue2-update`
  - `vue3-effect`: (数据驱动的)只有在对应的数据变化时，effect 副作用函数才会重新执行
  - `react-effect`: 要通过`setState`引起视图变化，且每次`render`时`effect`都会执行
  - `vue2-update`: 每次任何属性变化都会触发执行
