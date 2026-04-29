# Day 3: NumPy Basics

## 1. 导入
```python
import numpy as np
```
## 2. Create Arrays 创建数组
NumPy 里创建数组的方法有很多.np.array() 是最基础、最常用的创建方式.
```python
import numpy as np

array1 = np.array([1,2,3,4,5,6])
print(array1)
array2 = np.array([[1,2,3],[4,5,6]])
print(array2)
```
### 一些其他函数
`np.arange(0,20,2)` 指定取值范围和跨度

`np.linshape(2,6,15)` 在2-6区间里等距生成15个数

`np.random.rand(15)` 生成15个小数,默认范围是[0,1)

`np.ones((2, 2))` 全是1的数组

`np.zeros((2, 3))` 全是0的数组

## 2. Attribute 属性
### shape 看数组形状
````python
import numpy as np
array2 = np.array([[1,2,3],[4,5,6]])
print(array2.shape)
````
### ndim 看数组维度
```python
import numpy as np
array1 = np.array([1, 2, 3])
array2 = np.array([[1, 2, 3], [4, 5, 6]])
print(array1.ndim)
print(array2.ndim)
```
### size 看数组元素个数
```python
import numpy as np
array2 = np.array([[1,2,3],[4,5,6]])
print(array2.size)
```
### dtype 看数组元素的数据类型
```python
import numpy as np
array2 = np.array([[1,2,3],[4,5,6]])
print(array2.dtype)
```
### T 转置
```python
import numpy as np
array2 = np.array([[1,2,3],[4,5,6]])
print(array2.T)
```

## 4. Indexing 索引

