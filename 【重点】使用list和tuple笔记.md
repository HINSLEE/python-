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
【补充1】list.pop()理解成在栈中推出最后（最顶）的那个数据，所以list.pop()会返回最顶部的数据
       可以用a=list.pop()去取那个数据
       
【重点用法2】
Python列表函数&方法
Python包含以下函数:
序号	函数
1	cmp(list1, list2)
比较两个列表的元素
2	len(list)
列表元素个数
3	max(list)
返回列表元素最大值
4	min(list)
返回列表元素最小值
5	list(seq)
将元组转换为列表
Python包含以下方法:
序号	方法
1	list.append(obj)
在列表末尾添加新的对象
2	list.count(obj)
【统计】某个元素在列表中出现的【次数】
3	list.extend(seq)
在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表）
4	list.index(obj)
从列表中找出某个值第一个匹配项的索引位置
5	list.insert(index, obj)
将对象插入列表
6	list.pop(obj=list[-1])
移除列表中的一个元素（默认最后一个元素），并且返回该元素的值
7	list.remove(obj)
移除列表中某个值的第一个匹配项
8	list.reverse()
反向列表中元素
9	list.sort([func])
对原列表进行排序

元组索引，截取【这里而是用的中括号 注意！！！截取的时候不要用小括号】
因为元组也是一个序列，所以我们可以访问元组中的指定位置的元素，也可以截取索引中的一段元素，如下所示：
元组：
L = ('spam', 'Spam', 'SPAM!')
Python 表达式	结果	描述
L[2]	'SPAM!'	读取第三个元素
L[-2]	'Spam'	反向读取；读取倒数第二个元素
L[1:]	('Spam', 'SPAM!')	截取元素
       
【补充2】删除列表元素
可以使用 del 语句来删除列表的元素，如下实例：
list1 = ['physics', 'chemistry', 1997, 2000]
print list1
del list1[2]
print "After deleting value at index 2 : "
print list1
以上实例输出结果：
['physics', 'chemistry', 1997, 2000]
After deleting value at index 2 :
['physics', 'chemistry', 2000]

【补充3】Python列表脚本操作符
Python 表达式	                   结果	描述
len([1, 2, 3])	                  3	长度
[1, 2, 3] + [4, 5, 6]	         [1, 2, 3, 4, 5, 6]	组合
['Hi!'] * 4	                   ['Hi!', 'Hi!', 'Hi!', 'Hi!']	重复
3 in [1, 2, 3]	                True	元素是否存在于列表中
for x in [1, 2, 3]: print x    	1 2 3	迭代

【补充4】Python列表截取
Python 表达式   描述
L[2]	     读取列表中第三个元素
L[-2]	   	读取列表中倒数第二个元素
L[1:]	    从第二个元素开始截取列表

【补充5】Python List list()方法
list() 方法用于将元组转换为列表。
注：元组与列表是非常类似的，区别在于元组的元素值不能修改，元组（tuple）是放在括号中，列表（list）是放于方括号中。
语法
list()方法语法：
list( tup )
【实例】
aTuple = (123, 'xyz', 'zara', 'abc');
aList = list(aTuple)
print "列表元素 : ", aList
以上实例输出结果如下：
列表元素 :  [123, 'xyz', 'zara', 'abc']



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

【tuple的不变】tuple所谓的“不变”是说，tuple的每个元素，指向永远不变。即指向'a'，就不能改成指向'b'，指向一个list，就不能改成指向其他对象，但指向的这个list本身是可变的！
