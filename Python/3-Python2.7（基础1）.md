# 第一课时
## 1.Python的第一个输出语句
> #!/usr/bin/Python   

> print("Hello,world. My name is M##M!")  

如果是最新的Python3.0，则使用代码：

> #!/usr/bin/python3

> print("Hello,my python world! M##M!")

tips:关于第一行代码的解释
> #!/usr/bin/Python   

只适用于Linux / Unix用户，用来指定脚步用什么解释器  
目的：告知操作系统执行此脚步的时候，调用 /usr/bin 下的Python 解释器  
这种情况相当于写死了Python路径，如果想要改良，
可以使用下面的代码作为代替:
> #!/usr/bin/env python  
 
此代码运行时，系统会先去env里面查找Python的安装路径，再调用对应路径下的解释器完成操作

*shell脚本中在第一行也有类似声明*

## Python简单介绍
**定义** ： 高层次结合了解释性，编译性，互动性和面向对象的脚本语言  
1.解释型语言：开发无编译环境，类似PHP语言  
2.互交式语言：可以在Python提示符 >>>  后直接执行代码  
3.面向对象语言：代码封装的编程技术  
4.初学者的语言：支持广泛的应用程序开发，从简单文字处理到WWW浏览器到游戏！  

## Python发展历史
1.Python 是由 Guido van Rossum 在八十年代末和九十年代初，在荷兰国家数学和计算机科学研究所设计出来的。

2.Python 本身也是由诸多其他语言发展而来的,这包括 ABC、Modula-3、C、C++、Algol-68、SmallTalk、Unix shell 和其他的脚本语言等等。

3.像 Perl 语言一样，Python 源代码同样遵循 GPL(GNU General Public License)协议。

4.现在 Python 是由一个核心开发团队在维护，Guido van Rossum 仍然占据着至关重要的作用，指导其进展。

5.Python 2.7 被确定为最后一个 Python 2.x 版本，它除了支持 Python 2.x 语法外，还支持部分 Python 3.1 语法。

## Python特点
1.易于学习  
2.易于阅读  
3.易于维护  
4.一个广泛的标准库
5.互动模式：可以从终端输入执行代码并且获得结果的语言，互动测试和调试代码片段
6.可移植:多平台移动
7.可扩展：如果你需要一段运行很快的关键代码，或者是想要编写一些不愿开放的算法，
你可以使用C或C++完成那部分程序，然后从你的Python程序中调用。   
8.数据库：提供所有主要的商业数据库的接口
9.GUI编程：Python支持GUI可以创建和移植到许多系统调用。   
10.可嵌入：你可以将Python嵌入到C/C++程序，让你的程序的用户获得"脚本化"的能力。   

