# myBlog
this is a blog for demo and learn security topics.
## 功能与路由设计

在开发博客之前，我们首先需要明确博客要实现哪些功能。

功能及路由设计如下：

1. 注册
    1. 注册页：`GET /register`
    2. 注册（包含上传头像）：`POST /register`
2. 登录
    1. 登录页：`GET /login`
    2. 登录：`POST /login`
3. 登出：`GET /logout`
4. 查看文章
    1. 主页：`GET /posts`
    2. 个人主页：`GET /posts/:author`
    3. 查看一篇文章（包含留言）：`GET /posts/:postId`
5. 发表文章
    1. 发表文章页：`GET /posts/`
    2. 发表文章：`POST /posts/create`
6. 修改文章
    1. 修改文章页：`GET /posts/:postId/edit`
    2. 修改文章：`POST /posts/:postId/edit`
7. 删除文章：`DELETE /posts/:postId`
8. 留言
    1. 创建留言：`POST /comments`
    2. 删除留言：`GET /comments/:commentId/remove`

由于我们博客页面是后端渲染的，所以只通过简单的 `<a>(GET)` 和 `<form>(POST)` 与后端进行交互，如果使用 jQuery 或者其他前端框架（如 Angular、Vue、React 等等）可通过 Ajax 与后端交互，则 api 的设计应尽量遵循 Restful 风格。

#### Restful

Restful 是一种 api 的设计风格，提出了一组 api 的设计原则和约束条件。

如上面删除文章的路由设计：

```
GET /posts/:postId/remove
```

Restful 风格的设计：

```
DELETE /posts/:postId
```

可以看出，Restful 风格的 api 更直观且优雅。

更多阅读：

1. http://www.ruanyifeng.com/blog/2011/09/restful
2. http://www.ruanyifeng.com/blog/2014/05/restful_api.html
3. http://developer.51cto.com/art/200908/141825.htm
4. http://blog.jobbole.com/41233/

