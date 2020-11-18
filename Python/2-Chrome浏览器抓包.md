# Chrome浏览器抓包
## 获取的数据长什么样？
我们上一课学习了  
1.什么是爬虫？—— 可以自动化抓取网页上的信息技术    
2.爬虫的工作原理？—— 模拟浏览器想服务器进行数据请求    
接下来就该聊聊这些抓回的数据了。
浏览器网页以HTTP技术，在其中，有很多种请求方式，例如：GET, POST, PUT, DELETE, HEAD, OPTIONS, TRACE  
不过其中最常见的就是 **GET** 与 **POST**    
> 在我们请求的URL中：
>  https://www.baidu.com/s?wd=%E8%8B%8D%E8%80%81%E5%B8%88&rsv_spt=1&rsv_iqid=0xad707ee600011b25&issp=1&f=8&rsv_bp=1&rsv_idx=2&ie=utf8&rqlang=cn&tn=baiduhome_pg&rsv_enter=0&oq=%25E8%258B%258D%25E8%2580%2581%25E5%25B8%2588&rsv_t=5d8eqNDy4ZpyUOz7ByzyIMYfH5Jc7861dr4CFQaY3WCiDnOpBLob6Eouk23%2F3L%2BTD46O&rsv_sug3=15&rsv_pq=996e776f0000df06&rsv_sug4=19123
> 在 ？ 之后的都是GET请求的参数  
> 参数以【键值对】形式实现  
> eg：wd=%E8%8B%8D%E8%80%81%E5%B8%88  
> 告诉百度，我们查和XXX相关的内容

## GET请求
了解了GET请求的内容，我们以后在Python中写GET请求的时候，直接在URL后面加一个？然后添加参数值就可以了。
> 例如：百度搜索李白，
> https://www.baidu.com/s?wd=李白
> 使用百度直接搜索和用上面的链接查询效果是一样的。

## POST请求
POST参数不在URL上面，会以Form表单形式将数据提交给服务器。
POST请求参数放在request body

## Request Header 请求头
在做HTTP请求的时候，除了提交一些参数外，  
还有一些定义HTTP请求的头部信息，  
例如：Accept、Host、cookie、User-Agent  
当做爬虫的时候，我们同样会使用到，  

> 在代码里面设置 cookie 告诉服务器我们就是在这个浏览器请求的会话.
> User-Agent 告诉服务器我们是浏览器请求的.  
通过以上这些信息，伪装浏览器去欺骗服务器，伪装正规请求信息，爬取数据才能够成功！

## 服务器响应
有时页面访问常常出现404,502,200,301、、，这些都是服务器的响应码
一旦服务器访问，返回200，就说明请求成功！
![返回200](https://mmbiz.qpic.cn/mmbiz_png/J2icnQspGlaLtAfdZOuV2DZ2LRLQ4KVkKSOxe1WeUCP2IMNGXL52JehRPnXcUrJqz5pYGIWFiaXKjaxeeuHmkOvg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 响应头
当请求成功以后，服务器会给我们返回响应码外，还有响应头。
响应头：告诉我们数据以什么样的形式展现，cookie的设置
![响应头](https://mmbiz.qpic.cn/mmbiz_png/J2icnQspGlaLtAfdZOuV2DZ2LRLQ4KVkKyicGiarWPjOcq5V87BkialibSOPWuj2lib0OMSGHpvtgurWYUUiagmfZoOEw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)  
响应体：服务器返回的数据，点击Response，即可查看到  
![响应体](https://mmbiz.qpic.cn/mmbiz_png/J2icnQspGlaLtAfdZOuV2DZ2LRLQ4KVkKH71S6p24N0gKJ2MKeznvqL10vDAEYcl00xEaWsib05o2rmlibwQtPNNA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)  
响应体为服务器返回的HTML源代码、json、图片二进制代码等。  

# Sum：
总结一下，我们要去伪装请求，就先去研究正规请求的格式。
了解了GET、POST请求方式、知道请求头定义，知道怎么拿到返回的数据，爬虫技术就近在咫尺了。

