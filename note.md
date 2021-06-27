## 初始化项目

```bash
git clone git@github.com:vuejs/vue-next.git
rm -rf .git
git init
```

## 源码使用方式

1. 安装依赖

- 因为源码里用的是 `menorepo` 的规则，所以只能`yarn install`，不能`npm install`

2. 使用

- `npm run dev`默认找的是`packages/vue`包，并不是把所有包的方法都暴露在了全局下，当
- `yarn run build`把所有包都打包
