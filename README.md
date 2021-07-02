# Python
基础知识
用print()函数打印指定文字，把希望打印的文字用单引号或双引号括起来，print()遇到“，”会输出一个空格

用单引号或双引号括起来的叫字符串

用exit()退出Python

input()输入函数，可以让用户输入对应的字符串

布尔值：布尔值和布尔代数的表示完全一致，一个布尔值只有True,  False（注意大小写）两个值中一个

and（与运算）运算，只有所以都是True，and运算才是True

or（或运算）运算，只要其中有一个True,or运算就是True

not运算（非运算），可以把True变成False

None（空值），不能用0表示（0是有意义的），None是一个特殊空值

变量不能用数字开头，符号只能有“_”

/（除法）计算结果是浮点数，10/3=3.333333333335

//（地板除）计算结果是整数，10//3=3

%（余数）计算结果是余数，10%1=1

Python的浮点数没有大小限制，超过一定范围用inf（无限大）表示

8个比特（bit）作为一个字节（byte）,所以一个字节能表示的最大整数是255（二进制11111111=十进制255）

UTF-8编码

ord()函数获取字符的整数表示，chr()函数把编码转换为相应的字符

python的字符串类型是str，将str变为以字节为单位的bytes,bytes类型的数据用前缀带b的单引号或双引号表示：x =b’abc’,注意 ：’abc’和b’abc’前者是str,虽然内容一样，但是bytes的每个字节都只用一个字节

格式化：用%实现

%d 整数 %f 浮点数 %s 字符串 %x 十六进制整数

%s对任何数据类型取作用

'Hi, %s, you have $%d.' % ('Michael', 1000000)

'Hi, Michael, you have $1000000.'

显示单词"ada lovelace"

name = "ada lovelace"
print(name.title())以首字母大写的方式显示每个单词

print(name.upper())以全大写的方式显示每个单词
print(name.lower())以全小写的方式显示每个单词

绝对值函数 abs（）

\n 换行     \t 空格

str()将非字符串值表示为字符串,str不能直接与整数作比较，必须先把str转换为整数

if _name_ == ‘_nain_’:语句表示在一个.py文件中，如果运行该文件自身，那么_name_值就是‘_nain_’；如果它被别的文件导入的（该.py文件作为模板），则它的_name_就不是‘_nain_’。

所以if _name_ == ‘_nain_’中的命令只能在它独立运行时才执行

列表list：
用方括号（[]）来表示list，并用逗号来分隔其中的元素,list是可变序列，可以通过索引对元素取值，索引从零开始。

方法append()将元素'（‘’）'添加到了列表末尾

方法insert()可在列表的任何位置添加新元素。为此，你需要指定新元素的索引和值。insert(0, 'ducati')

如果知道要删除的元素在列表中的位置，可使用del语句

方法pop()可删除列表末尾的元素和列表中任意位置元素，并让你能够接着使用它。

你只知道要删除的元素的值，可使用方法remove()。

方法sort()永久性地修改了列表元素的排列顺序（按字母），只需向sort()方法传递参数
reverse=True反向排列

###要保留列表元素原来的排列顺序，同时以特定的顺序呈现它们，可使用函数sorted()，只需向sorted()方法传递参数reverse=True反向排列

要反转列表元素的排列顺序，可使用方法reverse()。与字母顺序无关

使用函数len()可快速获悉列表的长度

range()让你能够轻松地生成一系列的数字

min(digits)计算数列最小值
max(digits) 计算数列最大值
sum(digits) 计算数列总和

列表生成式：

list [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]可以用 list(range(1, 11))

[x * x for x in range(1, 11) if x % 2 == 0] 生成

[4, 16, 36, 64, 100]

 

生成器：
      一边循环一边计算的机制就是生成器（generator）

方法一：把一个列表生成式的[]改为（），就创建了一个generator

     L = [x * x for x in range(10)]

>>> L [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

>>> g = (x * x for x in range(10))

>>> next(g)

>>>0

for n in g:

... print(n)

生成器可以通过next()函数打印打印generator的下一个值

因为generator是可迭代对象，所以可以用for循环

方法二：如果一个函数中包含了yield关键字，那就是一个generator。执行过程中，遇到 yield就中断，下次又从yield处继续执行。

 

元组tuple:
       元组看起来犹如列表，但使用圆括号而不是方括号来标识。定义元组后，就可以使用索引来访问其元素，就像访问列表元素一样。Python将不能修改的值称为不可变的，而不可变的列表被称为元组。

      只有 1 个元素的 tuple 定义时必须加一个逗号,，来消除歧义:t = (1,)

 

切片：
     取一个list或tuple的部分元素。索引从0开始

     列：a[1,2,3,4,5,6]  a[ : 3]表示从索引0取到2（3-1）

也可以a[-2:]表示取最后两位数

 

字典dict
       在Python中， 字典是一系列键—值对。每个键都与一个值相关联，你可以使用键来访问与之相关联的值,这种key-value存储方式，可以通过key拿到对应的value，也可以在key中存放value,key必须是不可变对象。

列“alien_0 = {'color': 'green', 'points': 5}”

set
      set和dict类似，但只存储key，不存储value,且key不能重复，可以通过add(key)方法对set添加元素，重复添加同样的元素无效

        两个set可以做数学意义上的交集，并集

>>> s1 = set([1, 2, 3])

>>> s2 = set([2, 3, 4])

 >>> s1 & s2

{2, 3}

 >>> s1 | s2

{1, 2, 3, 4}

 

 

 

语句

if语句

     If-else语句   if-elif-else结构（可多次使用elif和省略else）

使用 break退出循环 

在循环中使用continue退出第一层循环

条件测试语句

while循环语句

     while x:  满足x条件语句就执行y语句

          y

for …. in …语句

 

with语句

 

 

惰性计算
迭代：
     给定一个 list 或 tuple，我们可以通过 for 循环来遍历这个 list 或tuple，这种遍历我们称为迭代（ Iteration）。通过for …. in来完成

通过 collections 模块的 Iterable 类型判断：

from collections import Iterable

>>> isinstance('abc', Iterable) # str 是否可迭代

enumerate 函数可以把一个 list 变成索引-元素对，这样就可以在 for 循环中同时迭代索引和元素本身

for i, value in enumerate(['A', 'B', 'C']):

    默认情况下， dict 迭代的是 key。如果要迭代 value，可以用 for  value in d.values()，如果要同时迭代 key 和 value，可以用 for  k, v in d.items()。

  for magician in magicians:

这行代码让Python获取列表magicians中的第一个，并将其存储到变量magician中

 

迭代器：
    可以直接用于for循环的对象统称为可迭代对象：Iterable。

可以被next()函数调用并不断返回下一个值的对象为迭代器：Iterator

可以用isinstance()判断一个对象是否是Iterator

>>>from collections import Iterator

>>>isinstance([],Iterator)

>>>False

把 list、 dict、 str 等 Iterable 变成 Iterator 可以使用 iter()函数：

>>> isinstance(iter([]), Iterator)

 

If语句    if-else语句   if-elif-else结构（可多次使用elif和省略else）

使用 break退出循环 

在循环中使用continue返回到循环开头

条件测试语句

 

函数
     函数本身可以赋值给变量，函数名也是变量

 用def开头 列

def  greet_user()：
"""显示简单的问候语"""
     print("Hello!")
greet_user()

from … import … as … 语句表示导入某.py文件中的某函数且对该函数改名

函数的返回值用return语句表示

pass语句：什么事也不做的空函数（占位符）

实参和形参

     形参函数完成其工作所需的一项信息。实参是调用函数时传递给函数的信息

 

map()函数
map()函数接收两个参数，一个函数，一个Iterable。map将函数依次作用到序列的每个元素，并把结果作为新的Iterator返回

>>> list(map(str, [1, 2, 3, 4, 5, 6, 7, 8, 9]))

['1', '2', '3', '4', '5', '6', '7', '8', '9']

 

reduce()函数
reduce 把一个函数作用在一个序列[x1, x2, x3, ...]
上，这个函数必须接收两个参数， reduce 把结果继续和序列的下一个元素做累积计算，其效果就是：

 reduce(f, [x1, x2, x3, x4]) = f(f(f(x1, x2), x3), x4)

 

filter()函数
     filter()函数用于过滤序列，接收一个函数一个序列，传入的函数依次作用于每个元素，然后根据返回的布尔值决定保留还是丢弃该元素

     def is_odd(n):

return n % 2 == 1

list(filter(is_odd, [1, 2, 4, 5, 6, 9, 10, 15]))

# 结果: [1, 5, 9, 15]

 

sorted()函数
     排序算法。

sorted()函数就可以对list进行从小到大的排列

此外，它还可以接收一个key函数来实现自定义排序

sorted([36, 5, -12, 9, -21], key=abs)

[5, 9, -12, -21, 36]

 

返回函数
函数作为返回值

def lazy_sum(*args):       >>>f = lazy_sum(1, 3, 5, 7, 9)

def sum():         >>> f

ax = 0        >>>f()

            for n in args:   >>>25

 ax = ax + n

return ax

return sum

返回的不是求和结果而是求和函数，调用f才打印求和结果

 

匿名函数
匿名函数 lambda  x:  x * x 实际上就是：

def  f(x):

return x * x

lambda表示匿名函数，冒号前面的x表示函数参数

匿名函数只能有一个表达式，不用return语句

 

装饰器
在代码运行期间动态增加功能的方式，称之为装饰器（Decorator）

def  addworld(func):

    def addfun():

       return func() + “world”

    return addfun

@addworld

def printhello():

   return “hello”

print printhello()

@addworld等价于addwold(printhello),意思是@X下面的函数作为X函数的参数（X也可是类）

 

偏函数
    当函数的参数太多，可以使用functools.partial（偏函数）

创建一个新函数，这个新函数可以固定原函数的部分参数，调用起来跟简单

>>> import functools

>>> int2 = functools.partial(int, base=2)  #把int设置为二进制转换十进制函数

 >>> int2('1000000')

64

>>> int2('1000000', base=10) #也可以在调用时传入其他值

 1000000

 

参数组合：
      位置参数：形参与实参必须一 一对应

默认参数（默认值）：每调用一次默认参数后默认参数的内容就被更新一次

      *args 是可变参数， args 接收的是一个 tuple；

     **kw 是关键字参数， kw 接收的是一个 dict。

     命名关键字参数：限制关键字参数的名字

def  person(*, city, job):  #限制了关键字参数的名字为city和job

     def  f1(a, b=0, *c, *, d, **e):

对于任意函数，都可以通过类似 func(*args, **kw)的形式调用

 

递归函数：
     如果一个函数在内部调用自己本身，这个函数就是递归函数。使用递归函数的优点是逻辑简单清晰，缺点是过深的调用会导致栈溢出。

列：n!可以这样写

   def fact(n):

      if  n == 1:

          return 1

      return  n * fact(n-1)

    在计算机中，函数调用是通过栈（ stack）这种数据结构实现的，每当进入一个函数调用，栈就会加一层栈帧，每当函数返回，栈就会减一层栈帧。由于栈的大小不是无限的，所以，递归调用的次数过多，会导致栈溢出。

 

模块：
     每一个包目录下面都会有一个__init__.py 的文件，这个文件是必须存在的

用import 打开模块 列 

     import pizza     代码行import pizza让Python打开文件pizza.py，并将其中的所有函数都复制到这个程序中。

     导入module_name.py文件中以function_name命名的函数：

     from module_name  import  function_name

使用 as 给函数指定别名  from  pizza  import  make _pizza  as  mp

上面的 import语句将函数 make_pizza()重命名为 mp()；

类
列class Dog(object)：#所有类最终都会继承的类object

      def  _init_ (self,name,age)

"""初始化属性name和age"""
self.name = name
self.age = age

def sit(self):
"""模拟小狗被命令时蹲下"""
print(self.name.title() + " is now sitting.")

def roll_over(self):
"""模拟小狗被命令时打滚"""
print(self.name.title() + " rolled over!")

以class开头 类的首字母大写，方法__init__()是一个特殊的方法 方法__init__()定义成了包含三个形参： self、 name和age。在这个方法的定义中，形参self必不可少，还必须位于其他形参的前面，调用时不用传达参数。

数据封装
在类的内部定义新的函数，使得数据封装在类中，类中的函数称为方法，比如方法sit（）和roll_over()

继承
   从现有的class继承，新的calss称为子类，被继承的class称为基类，父类或超类

class dog（Dog）:

pass

父类Dog，子类dog，继承最大的好处是可以获得父类的全部功能，且子类可以创建自己新的函数

多态
当子类与父类中含有相同函数时，子类的函数就覆盖了父类的函数

在继承关系中，子类的数据类型也可以被看做是父类

 

使用@property
     @property装饰器广泛应用在类的定义中，把一个getter方法变成属性，只需要加上@property就行了，另一个装饰器@score.setter，负责把setter方法变成属性赋值，通过getter和setter方法使属性不直接暴露，只定义getter方法，不定义setter就是一个只读属性

     class student(object):

         @property    #getter方法

         def score(self):

            pass

         @score.setter    #setter方法

         def score(self, value):

            pass

         @property

         def age(self):    #只读属性

            pass

 

多重继承
通过多重继承，一个子类就可以同时获得多个父类的所有功能

class Bat(Mammal, Flyable):

 pass

MixIn

    在定义类的过程中改变类的继承顺序，当某个模块不能修改时，通过MixIn方式可以动态添加该类的方法，动态改变类的原有继承体系

 

获取对象信息
使用type
判断数据类型

>>> type(123)   #判断基本数据类型

<class 'int'>

>>> type('str')

<class 'str'>

一个变量指向函数或类，也可以用typa()

比较两个变量数据类型是否相同

使用isinstance
判断class的类型可以使用isinstance（），可以判断一个对象是否是该类型本身，或者位于类型的父类继承链接上

使用dir（）
   获取一个对象的所有属性和方法

 

使用 _slots_
   由于程序运行的过程中可以动态给class加上方法，如果需要给class添加固定属性的方法，可以在定义class时，定义一个_slots_变量

 class Student(object):

__slots__ = ('name', 'age') # 用 tuple 定义允许绑定的属性名称

注意：使用_slots_定义的属性只对当前类起作用，对子类不起作用

 

定制类
形如_xxx_的变量或函数名在python中是有特殊用途的

_str_和_repr_
这两个方法都用于显示，当我们打印一个对象时显示的是对象的内存地址，我们可以用_str_或_repr_方法改变输出方式，_str_是面向用户的，而_repr_面向程序员

用_repr_方法时，不论直接输出对象还是用print打印的信息都会按照_repr_方法中定义的方式进行显示

用_str_方法时，直接输出对象不会按照_str_方法中定义的格式输出，只有print时才会

 

_iter_
   因为可直接使用for..in循环就是一个迭代对象，如果一个类被用于for..in循环，就必须用方法_iter_返回一个迭代对象，

for循环就会不断调用该迭代对象的_next_()方法拿到下一个值，如果_iter_方法返回的不是一个迭代对象或for循环结束就会报错

 

枚举类
python枚举作为一个类存在，使用他需要先导入枚举模块，然后继承并自定义需要的枚举类，导入模块可以是Enum(枚举值可以是任意类型)也可以是IntEnum（枚举值只能是整型）。枚举类的值不可以被外界更改

枚举类不允许存在相同的标签，但是允许不同标签的枚举值相同，这样后者相当于前者的别名，当使用了装饰器@unique后就不能设置别名了

from enum import Enum, unique 

@unique    #不能设置别名

class Weekday(Enum):  #继承Enum类

    sun = 0

 

错误处理
try的用法：
try:

print('try...')

r = 10 / int('2')

print('result:', r)

except ValueError as e:

print('ValueError:', e)

except ZeroDivisionError as e:

print('ZeroDivisionError:', e)

else:

 print('no error!')

finally:

print('finally...')

print('END')

当我们认为某些代码可能出错时，可以用try来运行该代码，try中从上往下执行一旦遇到错误代码就会直接跳入except语句（错误代码）中，并执行except后面为真的语句，如果try没有错误语句就不执行except而执行else语句，但不论怎样finally语句都会被执行，同样finally语句可有可无
