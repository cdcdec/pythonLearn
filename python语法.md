### python语法

##### 1.命令行执行文件
```
//在dos中执行python文件，格式：python 路径  文件名

C:\Users\cdc>python E:\python\Grammar\ggrammar.py   ggrammar.py
hello world

C:\Users\cdc>
```
##### 2.程序入口

```
if __name__ == '__main__':
```

##### 3.冒号与缩进

python使用冒号和代码缩进区分代码之间的层次。冒号代码之后的代码块需要缩进编写。

##### 4.导入模块（类或函数的集合）

import语句：导入模块，例如：import sys,则可以在代码中使用

```
import sys

print(sys.path)
print(sys.argv)
```

from...import..语句：导入某个模块中的一部分内容

```
from sys import path
from sys import argv

print(path)
print(argv)
```

##### 5.注释

单行注释：以#开头的内容为注释

##### 6.分号与语句分割

python倾向于使用换行作为每条语句的分割，但也支持使用分号作为语句的分割。也支持多行写一条语句，python使用"\"作为换行符。

```
sql="select id,name\"
     from dept\
     where name='A'"
 print(sql)
```

##### 7.变量

变量由数字、字母或下划线组成，变量的第一个字符必须是字母或下划线。python中的变量不需要声明,变量的赋值操作即室变量声明和定义的过程,一次新的赋值将创建一个新的变量，即使变量的名称相同，变量的标识并不相同。

```
x=1;
#打印出这个变量的标识
print(id(x))

#给多个变量赋值
a=(1,2,3)
(x,y,z)=a
print("x=",x)
print("y=",y)
print("z=",z)

#将两个变量的值互换
a=3
b=4
a,b=b,a
print(a)#输出4
print(b)#输出3
```

局部变量：只能在函数或代码段内使用的变量，作用范围只在其被创建的函数内有效.

全局变量：全局变量是能够被不同的函数、类或文件共享的变量，在函数之外定义的变量称为全局变量，其可以被文件内部的任何函数和外部文件访问。global关键字用于引用全局变量。

私有实例变量前必须有两个下划线。

常量：python没有提供定义常量的关键字。

##### 8数据类型

###### 8.1数字

数字类型分为整型、浮点型、布尔型、分数类型、复数类型。不需要声明变量的类型,python根据变量的值自动判断变量的类型。python内部没有普通类型，任何类型都是对象。可以使用type类,例如：

```
zhengxing=1
print(type(zhengxing))
#输出<class 'int'>

fd=1.23
print(type(fd))
#输出<class 'float'>

b=True   #不能写成true
print(type(b))
#输出<class 'bool'>

c=7+8j   #不能写成数学上的7+8i,会报错
print(type(c))
#输出<class 'complex'>
```

###### 8.2字符串

三种表示字符串的方式：单引号，双引号，三引号。其中单引号和双引号是等价的.三引号中可以输入单引号，双引号或换行符。转义操作只要在特殊字符的前面加上“\”即可。

##### 9运算符和表达式

###### 9.1算术运算符

四则运算符,求模运算符(x%y),求幂运算符(x**y).python不支持自增和自减运算符。

python算术表达式具有结合性和优先性，即从左到右，先乘除后加减。优先执行括号内的，再按照结合性执行.

######9.2关系运算符

关系运算符：大于(>),小于(<),大于等于(>=),小于等于(<=),等于(==),不等于(!=)。

大于(>),小于(<),大于等于(>=),小于等于(<=)优先级相同，等于(==),不等于(!=)优先级相同，且前者的优先级大于后者的优先级。

###### 9.3逻辑运算符

逻辑与(and),逻辑或(or),逻辑非(not)。

逻辑非的优先级大于逻辑与和逻辑或的优先级，而逻辑与和逻辑或的优先级相同。逻辑元算符的优先级低于关系运算符。

##### 10控制语句

###### 10.1条件语句

```
if(表达式):
缩进 语句1
else:
缩进 语句2


if(表达式1):
缩进 语句1
elif(表达式2):
缩进 语句2
elif(表达式3):
缩进 语句3
elif(表达式4):
缩进 语句4
else:
缩进 语句5

## if语句可以嵌套
```

###### 10.2循环语句

```
#while循环
while(表达式):

#带else的while循环
while(表达式):
缩进  语句
else:
缩进  语句

#for循环
for 变量 in  集合
   ...
else:
   ...
 
for x in range(-1,2):
    if(x>0):
        print("整数:",x)
    elif(x==0):
        print("零",0)
    else:
        print("负数",x)
else:
    print("循环结束");
   
```

###### 10.3break和continue语句

```
break语句：使程序跳出循环语句,从而执行循环之外的程序,即提前结束循环.
continue语句：只跳出当前的循环,然后继续执行后面的操作.
```

> 示例 冒泡排序
>
> ```
> def bubbleSort(numbers):
>         for j in range(len(numbers)-1,-1,-1):
>             for i in range(j):
>                 if(numbers[i]>numbers[i+1]):
>                     #将小的数放在前面
>                     numbers[i],numbers[i + 1]=numbers[i+1],numbers[i]
>                     print(numbers)
>
> def main():
>     numberss=[23,12,9,15,6]
>     bubbleSort(numberss)
>
> if __name__ == '__main__':
>     main()
> ```
>
> 