# 在项目中使用 Proxy 

修改配置文件 `.roadhogrc`

```diff
  {
    ...
+   "proxy": "./proxy.config.js"
    ...
  }
```

新增文件 `proxy.config.js`

```js
// 样例
// /api/users => http://jsonplaceholder.typicode.com/user
module.exports = {
  "/api": {
    "target": "http://jsonplaceholder.typicode.com/",
    "changeOrigin": true,
    "pathRewrite": { "^/api" : "" }
  }
};
```

## 详细说明

[webpack-dev-server#proxy](https://webpack.github.io/docs/webpack-dev-server.html#proxy)

