# HỌC PYTHON

## Data types:

### 1. Fundamental Data Types:

- int (integer) 

- float (floating point number)

- complex (real number)

- bool

- str

- list

- tuple

- set

- dict
  
  

```python
#<class 'int'>
print(type(2 + 4))

#<class 'float'>
print(type(3 / 5))

#<class 'float'>
print(type(5.0000001))

# Lấy mũ
print(2 ** 3) #8

# Chia lấy phần nguyên
print (5 // 4) #1

# Chia lấy phần dư
print (9 % 2) #1

print(bin(5)) #0b101
print(int('0b101', 2)) #5
```

### 2. Classes -> Custom Types

### 3. Specialized Data Types (Extra boost)

    - Modules

### 4. None

## Math functions

```python
print(round(3.1)) #3
print(round(3.9)) #4
print(abs(-1)) #1
```

## Operator precedence

```python
print(20 - 3 * 4) #8
```

## Variable

```python
number = 123
print(number) #123
```

### Best pratices for defining variables:

- snake_case

- start with lowercase or underscore

- letters, numbers

- case sensitive

- don't write keywore

```python
user_name = "Hieu"
print(user_name) #Hieu
_user_name = "Hieu" # private variable

# re_assign
user_name = "Ha"
print(user_name) #Ha
```

### Constants

```python
PI = 3.14
print(PI)

PI = 0 #don't do that
print(PI) #0
```

### Dunders

```python
__debug__
__doc__
```

Don't name variable that starts with \_\_

### Multiple assign variables

```python
a,b,c = 1,2,3
print(a) #1
print(b) #2
print(c) #3
```