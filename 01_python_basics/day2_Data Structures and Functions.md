# Day2:  Data Structures and Functions 数据结构与函数

## 1. List 列表
用来存放多个元素的数据结构.
列表使用方括号 `[]` 来表示,多个元素用`,`隔开
```python
scores = [99,85,77,90,66,59]
print(scores)
```

### 访问列表元素
```python
scores = [99,85,77,90,66,59]
print(scores[0])
print(scores[1])
print(scores[-1])
```


### 列表长度
```python
scores = [99,85,77,90,66,59]
print(len(scores))
```

### 添加新元素
```python
scores = [99,85,77,90,66,59]
scores.append(100)
print(scores)
```

### 删除元素
```python
scores = [99,85,77,90,66,59]
scores.remove(59)
print(scores)
```
### 列表的其他方法
`insert` 插入元素

`pop` 默认删除列表中最后一个原色

`clear` 清空列表中的原色

`del` 删除元素 

`index` 查找某个元素在列表中的索引位置

`count` 统计一个元素在列表中出现的次数

`sort` 排序

`reverse` 反转

### 常见运算
```python
a = [1, 2]
b = [3, 4]

print(a + b)
print(a * 2)
print(2 in a)
print(a[0:2])
```

## 2. Tuple 元组
用来存储多个元素的数据结构. 使用圆括号 `()` 来表示

元组是不可变类型
```python
t1 = (3,5)
print(t1)
```

### 访问元素
```python
t1 = (3,5)
print(t1[0])
```
### 查看类型
```python
t1 = (3,5)
print(type(t1))
```
### 元组长度
```python
t1 = (3,5)
print(len(t1))
```
### 打包和解包
```python
#打包
a = 1,2,3,4
print(type(a))
print(a)

#解包
e,f,g,h = a
print(e)
print(e,f,g,h)
```

### 常见运算
```python
a = (1, 2)
b = (3, 4)

print(a + b)
print(a * 2)
print(2 in a)
print(a[0:2])
```

## 3. Set 集合
一种无序且不重复的数据结构.集合可以用花括号 `{}` 表示，也可以使用 `set()` 创建

集合中的元素必须是 hashable 类型

集合会自动去除重复元素. 输出结果中只会保留不重复的值

```python
a = {1,2,2,2,3,4,5}
b = set('hello')
print(a)
print(b)
```

### 添加元素
```python
a = {1,2,2,2,3,4,5}
a.add(9)
print(a)
```

### 删除元素
```python
a = {1,2,2,2,3,4,5}
a.remove(2)
a.discard(3)
print(a)
```

### 成员判断
```python
a = {1,2,2,2,3,4,5}
print(6 in a)
print(2 in a)
```

### 常见运算
#### Intersection 交集 
两个集合都有的元素
```python
a = {1, 2, 3}
b = {3, 4, 5}
print(a & b)
```

### Symmetric Difference 对称差集
两个集合中不重复的元素
```python
a = {1, 2, 3}
b = {3, 4, 5}
print(a ^ b)
```

### Union 并集
两个集合的所有元素
```python
a = {1, 2, 3}
b = {3, 4, 5}
print(a | b)
```

### Difference 差集
在第一个集合,但不在第二个集合
```python
a = {1, 2, 3}
b = {3, 4, 5}
print(a - b)
```

## 4. Dictionary 字典
由键值对组成的数据结构. 用花括号 `{}` 来表示.每个元素由`:`分隔的两个值构成, 前面的是键,后面的是值.
```python
person = {'name': 'Onion', 'age': '99', 'height':'160'}
print (person['name'])
```

### 添加
```python
person = {'name': 'Onion', 'age': '99', 'height':'160'}
person['addr'] = 1
print (person)
```

### 修改
```python
person = {'name': 'Onion', 'age': '99', 'height':'160'}
person['height'] = 165
print (person)
```

### 删除
```python
person = {'name': 'Onion', 'age': '99', 'height':'160'}
person.pop('height')
print (person)
```

### 查看键和值
```python
person = {'name': 'Onion', 'age': '99', 'height':'160'}
print(person.keys())
print(person.values())
```

## 5. Function Basics 函数基础
使用 `def` 来定义函数.  `return` 来返回函数的执行结果
```python
def fun():
    print("hello!")
fun()
```
### 参数
是在定义函数时写在括号里的变量
```python
def fun(name):
    print("hello,", name)
fun("Onion")
```
```python
def fun(a, b):
    print(a + b)
fun(3,6 )
```

### 返回值
`return` 来返回函数的执行结果
```python
def fun(a, b):
    return a + b
result = fun(3, 6)
print(result)
```
多个返回值
```python
def name_age():
    return "Onion", 99
name, age =name_age()
print(name)
print(age)
```

### 默认参数
```python
def fun(name="cC"):
    print("hello,", name)
fun()
fun("Onion")
```

### 局部变量
只在这个函数内部有效
```python
def fun():
    age = 99
    print(age)
fun()
```

## Example
```python
scores = [56,78,99,34,76,89,53,77,85,49]
def get_average(score_list):  #算平均数
    total = 0
    for score in score_list:
        total += score
    return total / len(score_list)

def get_max(score_list):   #找最高分
    max_score = score_list[0]
    for score in score_list:
        if score > max_score:
            max_score = score
    return max_score

def get_min(score_list):
    min_score = score_list[0]
    for score in score_list:
        if score < min_score:
            min_score = score
    return min_score

def count(score_list):
    count = 0
    for score in score_list:
        if score >= 60:
            count += 1
    return count

def level(score):
    if score >= 90:
        return "A"
    elif score >= 80:
        return "B"
    elif score >=60:
        return "C"
    else:
        return "D"


average = get_average(scores)
max_score = get_max(scores)
min_score = get_min(scores)
pass_count = count(scores)

print("平均分:", average)
print("最高分:", max_score)
print("最低分:", min_score)
print("通过人数:", pass_count)

for score in scores:
    print(score,":",level(score))
```