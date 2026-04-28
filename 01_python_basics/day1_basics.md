# Day1: Python Basics and Control Flow


## 1. Variables 变量
### 变量可以保存的数据类型
整数(int)、浮点型(float)、字符串(str)、布尔型(bool)

```python
name = "Onion"      #str
age = 99            #int
height = 160.5      #float
is_student = True   #bool
```

### 查看变量类型
```python
name = "Onion"     
age = 99          
height = 160.5     
is_student = True 
print(type(name))
print(type(age))
print(type(height))
print(type(is_student))
```

### 类型转换
```python
age = 99
print(type(age))

age = str(age)
print(type(age))
```

## 2. print()
`print()` 是输出函数,用于在 Python 中输出内容

```python
print("Hello, World!")
print("I am learning Python")
```

### 输出变量
```python
name = "Onion"
age = 99

print(name)
print(age)
```

### 输出多个内容
```python
name = "Onion"
age = 99

print("My name is", name)
print("I am", age, "years old.")
```

## 3. input()
`input()` 是输入函数,用于接受用户输入
```python
name = input("请输入姓名: ")
print("Hello,", name)

age = input("Enter your age: ")
print(type(age))
```
默认返回的是字符串,即使输入的是数字,也是默认当字符串

### 类型转换
```python
age = int(input("请输入年龄: "))
height = float(input("请输入身高: "))
```

## 4. Operations 运算
### 常见基本运算符
`+` 加法
`-` 减法
`*` 乘法
`/` 除法
`//` 整除
`%` 取余
`**` 幂运算
```python
x = 12
y = 5

print(x + y)
print(x - y)
print(x * y)
print(x / y)
print(x // y)
print(x % y)
print(x ** y)
```

### 比较运算符
用来比较两个值

`==`等于 `!=`不等于 `>`大于 `<`小于 `>=`大于等于 `<=`小于等于
```python
x = 12
y = 5
print("x == y: ", x == y)
print("x != y: ", x != y)
print("x > y: ", x > y)
print("x < y: ", x < y)
print("x >= y: ", x >= y)
print("x <= y: ", x <= y)
```

### 逻辑运算符
用来组合多个条件

`and`并且 `or`或者 `not`不是
```python
age = 99
is_student = True
print("age > 18 and is_student: ", age > 18 and is_student)
print("age > 18 or is_student:", age > 18 or is_student)
print("not is_student:", not is_student)
```
## 5. 分支结构
### Conditional Statements 条件语句
进行条件判断和选择, 最常见的条件语句是 `if`

```python
age = 99
if age > 18: 
    print("成年人")
```

### if...else
有两种情况时可以用else
```python
age = int(input("请输入年龄: "))
if age >= 18: 
    print("成年人")
else: 
    print("未成年")
```

### if...elif
有多个条件时可以用elif,意思的否则如果
```python
age = int(input("请输入年龄: "))
if age > 35 and age <= 60:
    print("中年")
elif age >= 18 and age <=35:
    print("青年")
elif age > 60:
    print("老年")
else:
    print("未成年")
```
Notes: if后面要跟条件. if、else、elif后面要有冒号. 代码块要缩进.

## 6.循环结合
### -1 for Loop for循环
`for` 循环用来依次遍历列表中的每一个元素

```python
for i in range(10):
    print(i)
```

#### 在列表中使用for
```python
scores = [99,85,77,90,66,59]

for score in scores:
    print(score)
```

#### 在for中结合if
```python
scores = [99,85,77,90,66,59]

for score in scores:
    if score >= 60 :
        print(score,"合格")
    else:
        print(score,"不合格")
```
#### 字符串
```python
for char in "Python": 
    print(char)
```

### -2 while Loop while循环
`while` 循环会在条件成立时一直执行
```python
score = 2
while score <= 10:
    print(score)
    score += 1
```

### -3 break and continue
`break` 和 `continue` 用来控制循环

#### `break` 语句用于立即终止循环
```python
for i in range(10):
    if i ==6:
        break
    print(i)
```
#### `continue` 语句用于跳过当前这一次循环，直接进入下一次循环
```python
for i in range(10):
    if i ==6:
        continue
    print(i)
```
```python
scores = [99,85,77,90,66,59]

for score in scores:
    if score < 60 :
        continue
    print(score,"合格")
```
