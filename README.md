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
    2. 发表文章：`POST /posts`
6. 修改文章
    1. 修改文章页：`GET /posts/:postId`
    2. 修改文章：`PUT /posts/:postId`
7. 删除文章：`DELETE /posts/:postId`
8. 留言
    1. 创建留言：`POST /comments`
    2. 删除留言：`DELETE /comments/:commentId`

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

