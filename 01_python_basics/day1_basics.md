# Day1: Python basics
今天主要学习基础语法,包括变量,`print()`、`input()` 以及基本运算。

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

## 4. Basic Operations 基本运算
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