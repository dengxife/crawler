# http协议

1. http是超文本传输协议的缩写
2. http协议永远都是客户端发起的请求，服务端响应
3. http协议是一个无状态的协议（同一个客户端的这次请求和上次请求是没有对应关系的）
4. http协议是单向的
5. http协议是一个纯文本的协议

**特点**

1. 简单快速：只用传递请求方法和路径
2. 灵活：http可以传递任一类型的数据对象，通过content-type指定
3. 无连接：无连接意味着每次连接处理一个请求，服务器返回后断开连接，节省传输时间和服务器压力
4. 无状态：是指协议对于事务处理没有记忆，需要通过cookie和session来加以区别
5. 支持BS和CS模式

**http协议格式**

请求方法/空格/URL/空格/协议版本/回车符/换行符

头部字段名/:/值/回车符/换行符

...

头部字段名/:/值/回车符/换行符

回车符/换行符

请求数据

```http
GET / HTTP/1.1
Accept: text/html, application/xhtml+xml, image/jxr, */*
Accept-Language: zh-Hans-CN,zh-Hans;q=0.8,en-US;q=0.5,en;q=0.3
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; Trident/7.0; rv:11.0) Gecko
Accept-Encoding: gzip, deflate
DNT: 1
Host: image.baidu.com
Connection: Keep-Alive
Cookie: BAIDUID=88F7375808FD1AB609482C2897B35799:FG=1; 
```

**content-type**

application/x-www-form-urlencoded

浏览器的原生 form 表单，如果不设置 enctype 属性，那么最终就会以 application/x-www-form-urlencoded 方式提交数据。提交的数据按照 key1=val1&key2=val2 的方式进行编码，key 和 val 都进行了 URL 转码

multipart/form-data

使用表单上传文件时，必须让 form 的 enctype 等于这个值

application/json

告诉服务端消息主体是序列化后的 JSON 字符串