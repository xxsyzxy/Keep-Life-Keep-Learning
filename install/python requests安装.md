# Python Requests库安装
在安装中，我也遇到了一些问题：

## 1.问题
在安装了python以后，进入cmd（以管理员身份运行），进行requests库的安装

输入`pip install requests`
即可自动进行安装
安装以后，因为提升我有新版本可以替代，并给了我一行代码，我就直接运行了新代码
没想到的是，运行新代码以后，之前安装的库就出现了问题。
当我再次输入`import requests`的时候，
直接提示报错，报错信息如下：

```
Traceback (most recent call last):   
File "<pyshell#0>", line 1, in <module>     
import requests 
ModulNotFoundError:No module named 'requests'
```
## 2.报错原因
后面经过上网查找，了解到估计是因为某些原因，requests库并没有安装成功

## 3.解决方法
故，在cmd里面，再次输入`pip install requests`
在安装成功以后，我打开cmd，输入python，
在看到`>>>`以后，输入`import requests`，完美跳转到下一行`>>>`
则问题requests库安装问题得到圆满解决，接下来就是爬虫语法的学习了！
