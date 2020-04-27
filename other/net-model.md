ISO/OSI 七层网络参考模型:
|ISO/OSI 七层|TCP/IP 四层|
|:--:|:--:|
|应用层|应用层|
|会话层|
|表示层|
|传输层|传输层|
|网络层|网络层|
|数据链路层|网络接口层|
|物理层|

> TCP/IP 就相当于把 ISO/OSI 的应用层、表示层、会话层压缩为应用层；把数据链路层、物理层合并为网络接口层（更简单点网络接口层可以认为就是网卡）。压缩倾向于说把表示层和会话层的头部给砍掉了，然后其功能也部份砍掉了，合并倾向于说物理层的头部砍掉了但要实现的功能还是实现的。

各层之间的协议:
![图片](https://images2018.cnblogs.com/blog/1116722/201808/1116722-20180831152726586-1216033869.png)

数据封装:
![数据分装](https://images2018.cnblogs.com/blog/1116722/201808/1116722-20180831142744701-914791513.png)

网络请求：`GET`,`POST`,`PUT`,`HEAD`,`DELETE`,`OPTIONS`,`PATCH`,....

`GET`: 数据以键值对的方式拼接在 url 后面，例如：`https://www.test.com/login?username=wxling&password=123456`
`POST`:传参使用请求体时注意,`Content-type`常用两种类型:

1. `x-www-form-urlencoded`:数据同样是使用`key-value`键值对的方式进行拼接,`key=value&key1=value1&key2=value2..`
2. `form-data`