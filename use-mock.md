# 怎样在项目中使用 Mockjs (虚拟数据)

在项目开发过程中，前后端开发有时候速度不一样，在制作界面的时候缺乏数据或者在测试程序时，`Mockjs` 就派上用场了。

## 安装 Mockjs

```bash
$ npm i -D mockjs
```

## 配置命令

**以用户列表命令为例**

获取用户列表命令 `/api/getusers`

1. 新增文件 `mock/user.js`

  ```js
  import Mock from 'mockjs';
    
  export const getUser = ( req, res ) => {
    res.type('text');
    res.json(
      Mock.mock( {
        state: {
          'return': 'true',
          info: ''
        },
        'data|10-30': [ {
          'id|+1': 1
        } ]
      } )
    );
  }
  ```
    
2. 编辑 `.roadhogrc.mock.js`
   
  ```js
  import { getUsers } from './mock/user';
   
  export default {
    'GET /api/getusers': getUsers
  };
  ```

3. 启动服务打开浏览器访问 `127.0.0.1:8000/api/getusers` 看到数据配置成功。


