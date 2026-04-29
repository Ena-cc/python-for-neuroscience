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
### 普通索引
```python
import numpy as np
array1 = np.arange(1, 10)
print(array1[0])
print(array1[-1])
```
### 切片索引
[开始索引:结束索引:跨度(默认1)]
[start:end:step]
```python
import numpy as np
array2 = np.array([[1,2,3],[4,5,6],[7,8,9]])
print(array2[:2:1])
print(array2[0:2, 1:3]) #取第0到第1行 取第1到第2列

array3 = np.array([1, 2, 3, 4, 5])
print(array3[:3])    # 从开头取到索引 3 之前
print(array3[2:])    # 从索引 2 取到最后
print(array3[:])     # 全部
print(array3[::2])   # 每隔 2 个取一个
print(array3[::-1])  # 倒序
```

### 布尔索引
```python
import numpy as np
array1 = np.array([1, 2, 3, 4, 5])
print(array1>3)
print((array1>2) & (array1 <4))
```

## 练习
```python
import numpy as np
scores = np.array([56,78,99,34,76,89,53,77,85,49])
print("前三个成绩为:", scores[0:3])
print("后三个成绩为:", scores[-3:])
scores1 = scores[scores>80]
print ("大于80的分数:", scores1)
score2 = scores[scores<60]
print("小于60的分数:", score2)
scores_copy = scores.copy()
scores_copy[scores_copy < 60] = 60
print("低于60 改成60后:", scores_copy)

array2 = np.array([[1,2,3],[4,5,6],[7,8,9]])
print("第二行为:", array2[1,:])
print("第三列为:", array2[:,2])
print("取出数字5:", array2[1,1])
print("右下角2*2的区域:", array2[1:,1:])
print("取出所有大于5的数字:", array2[array2 > 5])
```

## 5. 数组运算
### 数组和数字的运算
```python
import numpy as np
np.random.seed(42)
array1 = np.random.rand(20)
print(array1)
print(array1 + 1)
print(array1 * 2)
print(array1 / 2)
```
### 数组和数组的运算
```python
import numpy as np
array1 = np.array([1,2,3])
array2 = np.array([4,5,6])
print(array1 + array2)
print(array1 - array2)
print(array1 * array2)
print(array1 / array2)

array3 = np.array([[1,2,3],[4,5,6],[7,8,9]])
print(array3 + 10)
print(array1 + array3)
```

## 6.常用方法
### 描述统计
```python
import numpy as np

scores = np.array([56, 78, 99, 34, 76, 89, 53, 77, 85, 49])

print("平均分:", scores.mean())
print("最高分:", scores.max())
print("最低分:", scores.min())
print("总分:", scores.sum())
print("标准差:", scores.std())
print("方差:", scores.var())
```
区分方法和函数
`scores.mean() == np.mean(scores)`

`scores.max()  == np.max(scores)`

`scores.min()  == np.min(scores)`

`scores.sum()  == np.sum(scores)`

`scores.std()  == np.std(scores)`

`scores.var()  == np.var(scores)`

### axis参数
表示沿那个方向进行统计
`array.mean(axis=0)` 表示按列计算，结果是每一列的平均值
`array2.mean(axis=1)`表示按行计算，结果是每一行的平均值

## 7. np.where 条件替换
根据条件对数组中的元素进行替换

`np.where(条件, 条件成立时的值, 条件不成立时的值)`

```python
import numpy as np

scores = np.array([56, 78, 99, 34, 76, 89, 53, 77, 85, 49])
scores2 = np.where(scores > 60, scores, 60)
print("修改后:", scores2)

scores3 = np.where(scores > 60, "pass", "fail")
print(scores3)

scores_grade = np.where(
    scores >= 85, "A",
    np.where(scores >= 75, "B",
             np.where(scores >= 60, "C","D"))
)
print(scores_grade)
```



