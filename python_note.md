# Python Note
***
## 数据类型
### 1. Number
支持int、float、bool、complex四类数字，相较python2，去除了Long长整型，int包含该类。
#### 数值计算
```
>>> 5 + 4  # 加法
9
>>> 4.3 - 2 # 减法
2.3
>>> 3 * 7  # 乘法
21
>>> 2 / 4  # 除法，得到一个浮点数
0.5
>>> 2 // 4 # 除法，得到一个整数
0
>>> 17 % 3 # 取余
2
>>> 2 ** 5 # 乘方
32
```
1. Python可以同时为多个变量赋值，如a, b = 1, 2。
2. 一个变量可以通过赋值指向不同类型的对象。
3. 数值的除法包含两个运算符：/ 返回一个浮点数，// 返回一个整数。
4. 在混合计算时，Python会把整型转换成为浮点数。
| :int: | :float: | :complex: |
| 10	| 0.0	| 3.14j |
| 100 |	15.20 |	45.j |
-786	-21.9	9.322e-36j
080	32.3e+18	.876j
-0490	-90.	-.6545+0J
-0x260	-32.54e100	3e+26J
0x69	70.2E-12	4.53e-7j

2. String
3. List
4. Tuple
5. Set
6. Dictionary

***
## 备注
1、2、4为不可变数据<br>
常用type()判断类型，也可用isinstance(ele,int)判断，区别在instance()会认为子类是一种父类，而type()不会
```python
>>> class A:
...     pass
... 
>>> class B(A):
...     pass
... 
>>> isinstance(A(), A)
True
>>> type(A()) == A 
True
>>> isinstance(B(), A)
True
>>> type(B()) == A
False
```
在Python2中，以0、1代表True与False，Python3中将两者定为关键字，但值仍旧为1与0，可以与数字进行计算。
