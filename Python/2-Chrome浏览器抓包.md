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
