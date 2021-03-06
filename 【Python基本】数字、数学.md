# python-

一、Python Number 类型转换
int(x [,base ])         将x转换为一个整数  
long(x [,base ])        将x转换为一个长整数  
float(x )               将x转换到一个浮点数  
complex(real [,imag ])  创建一个复数  
str(x )                 将对象 x 转换为字符串  
repr(x )                将对象 x 转换为表达式字符串  
eval(str )              用来计算在字符串中的有效Python表达式,并返回一个对象  
tuple(s )               将序列 s 转换为一个元组  
list(s )                将序列 s 转换为一个列表  
chr(x )                 将一个整数转换为一个字符  
unichr(x )              将一个整数转换为Unicode字符  
ord(x )                 将一个字符转换为它的整数值  
hex(x )                 将一个整数转换为一个十六进制字符串  
oct(x )                 将一个整数转换为一个八进制字符串  

二、Python math 模块、cmath 模块
Python 中数学运算常用的函数基本都在 math 模块、cmath 模块中。
Python math 模块提供了许多对浮点数的数学运算函数。
Python cmath 模块包含了一些用于复数运算的函数。
cmath 模块的函数跟 math 模块函数基本一致，区别是 【cmath 模块运算的是复数，math 模块运算的是数学运算】。
要使用 math 或 cmath 函数必须先导入：import math
【实例】
查看 math 查看包中的内容:
>>> import math
>>> dir(math)
['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 
'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e',
'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 
'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 
'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
>>>

【cmath实例】
>>> import cmath
>>> cmath.sqrt(-1)
1j
>>> cmath.sqrt(9)
(3+0j)
>>> cmath.sin(1)
(0.8414709848078965+0j)
>>> cmath.log10(100)
(2+0j)
>>>

三、Python数学函数
【有些函数不能直接访问的，需要导入 math 模块，通过静态对象调用该方法】
【下面的不可直接调用的按这个格式写（以ceil函数为例）：
import math
math.ceil( x )】

函数	                                      返回值 ( 描述 )
abs(x)【可直接调用】	               返回数字的【绝对值】，如abs(-10) 返回 10
ceil(x)【不可】	                   返回数字的上入整数，如math.ceil(4.1) 返回 5【进一法得出整数】
cmp(x, y)【可】	                  如果 x < y 返回 -1, 如果 x == y 返回 0, 如果 x > y 返回 1
exp(x)【不可】	                   返回e的x次幂(e^x),如math.exp(1) 返回2.718281828459045
fabs(x)【不可】	                   返回浮点数字的【绝对值】，如math.fabs(-10) 返回10.0
floor(x)【不可】	                 返回数字的下舍整数，如math.floor(4.9)返回 4【退一法得出整数】
log(x)【不可】	                   如math.log(math.e)【math.log(真数,底数)】返回1.0,math.log(100,10)返回2.0
log10(x)【不可】	                 返回以10为基数的x的对数，如math.log10(100)返回 2.0
max(x1, x2,...)【可】	            返回给定参数的最大值，参数可以为序列。
min(x1, x2,...)【可】              返回给定参数的最小值，参数可以为序列。
modf(x)【不可】	                   返回x的整数部分与小数部分，两部分的数值符号与x相同，整数部分以浮点型表示。【返回格式为：小数部分 整数部分】
pow(x, y)【不可】                  返回x^y（x的y次幂）运算后的值。

内置的 pow() 方法
pow(x, y[, z])
函数是计算x的y次方，如果z在存在，则再对结果进行取模，其结果等效于pow(x,y) %z
注意：pow() 通过内置的方法直接调用，内置方法会把参数作为整型，而 math 模块则会把参数转换为 float。

round(x,n)【可】（x保留n位小数）	   返回浮点数x的四舍五入值，如给出n值，则代表舍入到小数点后的位数。
sqrt(x)【不可】                     返回数字x的平方根
