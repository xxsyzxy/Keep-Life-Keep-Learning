# 第二课时
## Python中文编码
Python输出英文“hello world”很正常，
但是如果输出的是“你好，世界！”就可能遇到中文编码问题而报错。
报错如下：
> File "test.py", line 2
> SyntaxError: Non-ASCII character '\xe4' in file test.py on line 2, but no encoding declared; 
> see http://www.python.org/peps/pep-0263.html for details

实际上，如果Python中没有指定编码，在执行过程中，就会出现报错！  
Python中，默认的编码格式是ASCII格式，在没有修改编码格式时，无法正确打印汉字。  
解决方法：在文件开头加入 

`# -*- coding:UTF-8 -*-`  

`# coding=utf-8`

全部代码如下：
```
#!/usr/bin/env python

# coding=utf-8

print("你好，世界！")

```

简而言之，如果代码中包含中文，那么我们就需要在头部进行编码。
> 我在想，如果是那种俄国、日本语、阿拉伯语，应该也需要进行相应编码，才可能打出不同的字符吧   
> 不过就是不知道是哪一种编码了？？

除此以外，Python3.X 源代码默认使用utf-8，可以进行正常的中文解析，所以无需在指定utf-8编码。
另外，如果使用编辑器，那么需要同时设置py文件存储格式为utf-8，否则会报错如下：
> SyntaxError: (unicode error) ‘utf-8’ codec can’t decode byte 0xc4 in position 0:
> invalid continuation byte

