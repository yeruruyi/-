---
* 记录笔记
* 记录人：叶倩
* 时间：2021.12.01
* week14（week08学习周）
* 本周参考资源：

---
# Auth methods
1.通过URL路径的信息传递验证身份
>1.在URL路径中提交验证信息
/basic-auth/{user}/{passwd}
Prompts the user for authorization using HTTP Basic Auth.
2.例如：
>> 1. user  = Lihua
 2. passwd = 123456
 3. 通用： URL = https://httpbin.org/basic-auth/{user}/{passwd}
 4. 本案例： URL = https://httpbin.org/basic-auth/Lihua/123456

2.例如：
>1.user=Lihua
2.passwd=123456
3.通用:URL=http://httpbin.org/basic-auth{user}/{passwd}
4.本案例:URL=http://httpbin.org/basic-wuth/Lihua/123456
2.通过访问需要验证的URL地址，填入正确的注册信息（user和passwd,
>1.200:

# Status codes
1.httpbin.org网络的测试URL为；http://httpbin.org/status/{codes}
2.状态码测试结果:
>1.http://httobin.org/status/100
>>1.informational(信息性状态码)-接收的请求正在处理---加载中...
 2.类型错误：无法获取
2.http://httpbin.org/status/200
>>1.Success(成功状态码)--请求正常处理完毕
 2.
3.http://httpbin.org/status/300
>>1.Redirection(重定向状态码)---需要进行附加操作以完成请求
 2.Status Code:300MULTIPLE CHOICES
4.http://httpbin.org/status/400
>>1.Clien Error(客户端错误状态码)---服务器无法处理请求
 2.无响应内容，请客户检查错误请求信息（URL）是否正确，或者请求方式（如GET，POST）是否正确
5.http://httpbin.org/status/500
>>1.Server Error(客户端错误状态码)---服务器无法处理请求
 2.服务器报错的处理方法，找到服务人员（如客服等)询问网站问题，服务端人员通过检查后端代码解决。
 
# 4.请求检查
1.检查首部信息
 >1.测试的URL路径：http://httpbin.org/headers
 2.返回页面信息是请求客户端的请求首部信息，结果如下：

2.检查**请求者**的ip地址：
>>1.测试的URL路径：http:/httpbin.org/ip
2.返回结果为:
 {
  "origin": "223.104.67.122"
}
3.检查请求者的网络代理
>1.测试的URL路径：http://httpbin.org/user-agent
2.返回测试的结果为：
```json
   > {
      "user-agent": "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36"
    }
    ```

# 5.图片信息
1.测试链接：http://httpbin.org/image
2.返回信息：一张测试图片
![img](http://httpbin.org/image)

 "iconPath": "天气"，
      "selectedIconPath": "天气"

 onLoad: function (options) {
        wx.request({
            url: 'http://aip.baidubce.com/oauth/2.0/token', //仅为示例，并非真实的接口地址
            data: {
                grant_type: 'client_credentials', // 这是固定值
                client_id: 'QuvXGOObs3vkiq4paLBfarSo', // 这是百度AI开放平台的token令牌认证
                client_secret: 'Bb7a1xhkqS1czG4RU3363NhToStqc1px'
            },
            header: {
              'content-type': 'application/json' // 默认值
            },
            success (res) {
              console.log(res.data)
            }
          })
    },
