参考

- [从输入URL到页面加载发生了什么？](https://segmentfault.com/a/1190000006879700)
- [从输入url到页面加载完成发生了什么？——前端角度](https://www.cnblogs.com/daijinxue/p/6640153.html)

- [DNS解析的过程是什么，求详细的？](<https://www.zhihu.com/question/23042131>)

整体上分为以下几个阶段:

- 输入URL,DNS解析URL对应IP
- 根据IP建立TCP连接
- 发送HTTP请求
- 服务器处理请求，浏览器接收HTTP响应
- 浏览器解析,渲染页面
- 关闭TCP连接

