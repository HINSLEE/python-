# python-

list：
Python内置的一种数据类型是列表：list。list是一种有序的集合，可以随时添加和删除其中的元素。

【重点用法】
len(list)：获取list元素的个数
list[x]：用索引来访问list中索引号为x的元素
list[-1]：list中倒数第一个元素
list.append()：往list中追加元素到末尾
list.insert(x,'...')：把...元素插入到索引号为x的位置中
list.pop()：删除list中最后一个元素
list.pop(x)：删除list中索引号为x的元素
list[x]='...'：把索引号为x的元素替换成...
list中的元素可以为一个新的list

>>> classmates = ['Michael', 'Bob', 'Tracy']
>>> classmates
['Michael', 'Bob', 'Tracy']

1、变量classmates就是一个list。用len()函数可以获得list元素的个数：
>>> len(classmates)
3

2、用索引来访问list中每一个位置的元素，记得索引是从0开始的：
>>> classmates[0]
'Michael'
>>> classmates[1]
'Bob'
>>> classmates[2]
'Tracy'

3、当索引超出了范围时，Python会报一个IndexError错误，所以，要确保索引不要越界，记得最后一个元素的索引是len(classmates) - 1。
如果要取最后一个元素，除了计算索引位置外，还可以用-1做索引，直接获取最后一个元素：
>>> classmates[-1]
'Tracy'

4、list是一个可变的有序表，所以，可以往list中追加元素到末尾：
>>> classmates.append('Adam')
>>> classmates
['Michael', 'Bob', 'Tracy', 'Adam']

5、也可以把元素插入到指定的位置，比如索引号为1的位置：
>>> classmates.insert(1, 'Jack')
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy', 'Adam']

6、要删除list末尾的元素，用pop()方法：
>>> classmates.pop()
'Adam'
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy']

7、要删除指定位置的元素，用pop(i)方法，其中i是索引位置：
>>> classmates.pop(1)
'Jack'
>>> classmates
['Michael', 'Bob', 'Tracy']

8、要把某个元素替换成别的元素，可以直接赋值给对应的索引位置：
>>> classmates[1] = 'Sarah'
>>> classmates
['Michael', 'Sarah', 'Tracy']

9、list里面的元素的数据类型也可以不同，比如：
>>> L = ['Apple', 123, True]

10、list元素也可以是另一个list，比如：
>>> s = ['python', 'java', ['asp', 'php'], 'scheme']
>>> len(s)
4
要注意s只有4个元素，其中s[2]又是一个list，如果拆开写就更容易理解了：
>>> p = ['asp', 'php']
>>> s = ['python', 'java', p, 'scheme']
要拿到'php'可以写p[1]或者s[2][1]，因此s可以看成是一个二维数组，类似的还有三维、四维……数组，不过很少用到。
如果一个list中一个元素也没有，就是一个空的list，它的长度为0：
>>> L = []
>>> len(L)
0


tuple：
另一种有序列表叫元组：tuple。tuple和list非常类似，但是tuple一旦初始化就不能修改，比如同样是列出同学的名字：
>>> classmates = ('Michael', 'Bob', 'Tracy')
现在，classmates这个tuple不能变了，它也没有append()，insert()这样的方法。其他获取元素的方法和list是一样的，你可以正常地使用classmates[0]，classmates[-1]，但不能赋值成另外的元素。

【tuple的陷阱】：当定义一个只有一个元素的tuple，要在括号里面写完元素后加上一个逗号，如：
>>> t = (1,)
>>> t
(1,)
这是因为括号()既可以表示tuple，又可以表示数学公式中的小括号，这就产生了歧义，因此，Python规定，这种情况下，按小括号进行计算，计算结果自然是1。
