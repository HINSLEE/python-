# python-

如果你输出中文字符"你好，世界"就有可能会碰到中文编码问题。
Python 文件中如果未指定编码，在执行过程会出现报错：

#!/usr/bin/python
print "你好，世界";

以上程序执行输出结果为：
  File "test.py", line 2
SyntaxError: Non-ASCII character '\xe4' in file test.py on line 2, but no encoding declared; see http://www.python.org/peps/pep-0263.html for details

Python中默认的编码格式是 ASCII 格式，在没修改编码格式时无法正确打印汉字，所以在读取中文时会报错。
解决方法为只要在文件开头加入 # -*- coding: UTF-8 -*- 或者 #coding=utf-8 就行了
注意：#coding=utf-8 的 = 号两边不要空格。
