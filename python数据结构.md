### python数据结构

####1.元组结构

##### 1.1创建元组

```
tuple=(元素1,元素2,...)
# 每个元素可以存储不同类型的数据。元组创建后不能对其中的元素再做任何修改操作。
tup1 = ()   #创建空元组
tup1 = (50,)   #创建只含有一个元素的元组,需要在元素后面添加逗号
#元组与字符串类似，下标索引从0开始，可以进行截取，组合等
#二元元组,即元组里面的元素也是一个元组
tuple=(('t1','t2'),('t3','t4'))

```

##### 1.2元组的访问

###### 1.2.1 tuple[n]

n的值可以是0，正整数或负整数。负数索引从元组的尾部开始计数,最后端的元素索引表示"-1",次尾端的元素索引表示"-2"。

###### 1.2.2 tuple[m:n]

m、n可以是0，正整数或负整数。tuple[m:n]表示从第m个索引到第n个索引(不包含第n个索引所指向的元素)所指定的所有元素。

###### 1.2.3  tuple [m]\[m]

用来访问二元元组

###### 1.2.4 打包与解包

```
#打包，元组的创建即打包的过程
tuple=('apple','banana','grape','orange')
#解包,元组中的四个元素分别赋值给左边的4个变量。
a,b,c,d=tuple
```

##### 1.3元组的遍历

```
#方法1
    for i in range(len(tuple)):
        print("tuple[%d]:"%i)
        for j in range(len(tuple[i])):
            print(tuple[i][j])
        #打印一个空行
        print()
#方法2
    for  i in tuple:#遍历元组
        for j in i:#遍历子元组
            print(j)#依次打印出元素
```

#### 2.列表结构

##### 2.1列表的创建

```
#列表的元素可以是元组、列表、字典或任何对象，同一个列表中元素的类型可以不同
    list=['apple','banana','grape','orange','watermelon']
    print(list)#打印列表
    list.append(1)#给列表添加元素
    list.remove(1);#列表删除元素,删除值为1的元素,如果没有这个元素会报错。如果列表中有两个值为1的元素，则会删除第一个值为1的元素。
    list.insert(1,12)#在原列表索引位置为1的地方加入一个元素
    print(list)
    print(list.pop())#打印列表中的最后一个元素,此时列表中最后一个元素会被弹出,即删除掉最后一个元素
    print(list)
```
##### 2.2列表的访问

###### 2.2.1 list[n]

n的值可以是0，正整数或负整数。负数索引从列表的尾部开始计数,最后端的元素索引表示"-1",次尾端的元素索引表示"-2"。

###### 2.2.2 list[m:n]

m、n可以是0，正整数或负整数。tuple[m:n]表示从第m个索引到第n个索引(不包含第n个索引所指向的元素)所指定的所有元素。

###### 2.2.3  list [m]\[m]

用来访问二元列表

###### 2.2.4 打包与解包

```
#打包，列表的创建即打包的过程
list=['apple','banana','grape','orange']
#解包,列表中的四个元素分别赋值给左边的4个变量。
a,b,c,d=list
```
##### 2.3列表的遍历

```
list3 = [['apple', 'banana'], ['grape', 'orange'], ['watermelon',]]
#方法1
     for i in range(len(list3)):
        print("list3[%d]:" % i)
        for j in range(len(list3[i])):
            print(list3[i][j])
        # 打印一个空行
        print()
#方法2
     for  i in list3:#遍历列表
        for j in i:  # 遍历子列表
            print(j)  # 依次打印出元素
```

##### 2.4列表的连接

调用列表的extend方法，或者使用运算符+，+=，*连接两个列表

```
list4=['app','ora','jik']
list5 = ['app2', 'ora2', 'jik2']
list4.extend(list5)   #list4连接list5,并形成一个新的列表list4
print(list4)
    
list6 = ['app3', 'ora3', 'jik3']

list5=list5+list6  #将list5与list6连接后赋给list5
print(list5)

list6+=['grape']
print(list6)  #使用+=给list6连接上['grape']

list7=['apple7','kklk7']*2   #连接了两个相同的列表
print(list7)
```

