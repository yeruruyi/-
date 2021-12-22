---
* 记录笔记
* 记录人：叶倩
* 时间：2021.11.24
* week13（week07学习周）
* 本周参考资源：
>1.
2.
3.
----
# HHTP Methods
## GET请求
* 1.不带参数的GET请求
测试的url：http://httpbin.org/get
Request(客户端)：GET http://httpbin.org/get HTTP1.1
Response(服务器)：
>1. Response body（输出请求客户的请求信息Request headers):
{
  "args": {}, 
  "headers": {
    "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9", 
    "Accept-Encoding": "gzip, deflate", 
    "Accept-Language": "zh-CN,zh;q=0.9,en;q=0.8,en-GB;q=0.7,en-US;q=0.6", 
    "Host": "httpbin.org", 
    "Upgrade-Insecure-Requests": "1", 
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Safari/537.36 Edg/96.0.1054.29", 
    "X-Amzn-Trace-Id": "Root=1-619e1ce8-5e4d2f00268b5f7770af3318"
  }, 
  "origin": "223.104.67.15", 
  "url": "http://httpbin.org/get"
}
2. Response headers
请求 URL: http://httpbin.org/get
请求方法: GET
状态代码: 200 OK
远程地址: 18.232.227.86:80
引用站点策略: strict-origin-when-cross-origin

* 2.带参数请求
 测试的url：http://httpbin.org/get
Request(客户端)：GET http://httpbin.org/get HTTP1.1
带参数的请求方式：http://httpbin.org/get +？+参数1名称=参数1值+&+参数2名称=参数2值+...
请求的主体和带着？后面的参数访问服务器，服务器可以对参数进行对应的处理（例如搜索浏览器查询内容之后进行反馈）


## 1.2 POST请求
* 1. 不带参数的POST请求
 测试的url：http://httpbin.org/get
Request(客户端)：GET http://httpbin.org/get HTTP1.1
请大家 点击 http://httpbin.org/post 试一试
结论：
* 1. 在浏览器上输入的url链接的方法是GET
* 2.  客户端是GET ------服务端是POST method not allowed
* 3. POST需要**提交表单**
Response(服务器)body(<font style="color":red>观察数据中除了"args"多出了："data","files","form"):
{
  "args": {},
  "data": "",
  "files": {},
  "form": {},
  "headers": {
    "Accept": "application/json",
    "Accept-Encoding": "gzip, deflate",
    "Accept-Language": "zh-CN,zh;q=0.9,en;q=0.8,en-GB;q=0.7,en-US;q=0.6",
    "Content-Length": "0",
    "Host": "httpbin.org",
    "Origin": "http://httpbin.org",
    "Referer": "http://httpbin.org/",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Safari/537.36 Edg/96.0.1054.29",
    "X-Amzn-Trace-Id": "Root=1-619e25ac-69f69c4f0fd004bd7eaac263"
  },
  "json": null,
  "origin": "223.104.67.15",
  "url": "http://httpbin.org/post"
}
* 2.Respnose headers (服务器的HTTP特征描述)
 access-control-allow-credentials: true 
 access-control-allow-origin: http://httpbin.org 
 connection: keep-alive 
 content-length: 671 
 content-type: application/json 
 date: Wed, 24 Nov 2021 11:44:44 GMT 
 server: gunicorn/19.9.0 
 status:200
