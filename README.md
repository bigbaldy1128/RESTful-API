# RESTful API
关于RESTful API，这一片文章就够了：[《Principles of good RESTful API Design》](https://codeplanet.io/principles-good-restful-api-design/)，以下内容只是简单提炼，想深入学习的请阅读[《REST in Practice》](https://pan.baidu.com/s/1kVIge9L)，
## 动词
* GET (SELECT) - 从服务器检索特定资源，或资源列表。
* POST (CREATE) - 在服务器上创建一个新的资源。
* PUT (UPDATE) - 更新服务器上的资源，提供整个资源。
* PATCH (UPDATE) - 更新服务器上的资源，仅提供更改的属性。
* DELETE (DELETE) - 从服务器删除资源。
* HEAD - 检索有关资源的元数据，例如数据的哈希或上次更新时间。
* OPTIONS - 检索关于客户端被允许对资源做什么的信息。
## 预期的返回文档
* GET /collection：返回资源对象的列表
* GET /collection/resource：返回单个Resource对象
* POST /collection：返回新创建的Resource对象
* PUT /collection/resource：返回完整的Resource对象
* PATCH /collection/resource：返回完整的Resource对象
* DELETE /collection/resource：返回一个空文档
## 例子
|Verb|URI|Use|
|----|---|---|
|POST|/project|新建项目|
|GET|/project/{pkpj}|查询一个项目|
|GET|/project|查询所有项目|
|DELETE|/project/{pkpj}|删除一个项目|
|PUT|/project/{pkpj}|更新一个项目|
|GET|/project/{pkpj}/code|查询某个项目下的所有代码|

## 基本原则
* 网址中不能有动词，只能有名词
* API版本信息添加到URL中，例如v1/project（或将版本信息放到HTTP请求头的accept字段中）
* 超媒体API（Hypermedia）：返回结果提供链接对应下一步的API，即使用户不查文档，也知道下一步该做什么

## 参考资料
* http://www.ruanyifeng.com/blog/2011/09/restful.html
* http://www.ruanyifeng.com/blog/2014/05/restful_api.html
* https://zhuanlan.zhihu.com/p/24592119