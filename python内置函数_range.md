### python内置函数_range

> Python3.x 中 range() 函数返回的结果是一个整数序列的对象,<class 'range'>,不是列表，但是可以利用 list 函数返回列表,即list(range(10))

##### 1.函数说明

```
range(start, stop[, step])
start: 计数从 start 开始。默认是从 0 开始。例如range（5）等价于range（0， 5）;
end: 计数到 end 结束，但不包括 end。例如：range（0， 5） 是[0, 1, 2, 3, 4]没有5
step：步长，默认为1。例如：range（0， 5） 等价于 range(0, 5, 1)
```

