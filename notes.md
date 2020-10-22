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

## Expression

is a piece of code that produce a value

## Statement

is an entire line of code

## Augmented assignment operator

```python
some_value = 5
some_value += 2
some_value -= 3
some_value *= 2
some_value /= 2
```

## String

```python
type('hello world') #<class 'str'>
type("hello world again") #<class 'str'>

username = 'account@gmail.com'
password = 'secretpassword'
long_string = '''
WOW
0 0
---
'''

print(long_string)

first_name = 'Hieu'
last_name = 'Nguyen Trong'
full_name = first_name + ' ' + last_name
print(full_name) # Nguyen Trong Hieu
```

## String concatenation

Adding string together

```python
print('hello' + ' ' + 'Hieu!') # hello Hieu!
print('hello' + 5) #error
```

## Type conversion

```python
print(type(str(100))) #<class 'str'>
print(type(int('100'))) #<class 'int'>
```

## Escape Sequence

```python
weather = 'It\'s sunny'
weather_1 "It's sunny"
weather_2 = '''It's sunny'''
tab = '\t'
newline = '\n'
```

## Formatted strings

```python
name = 'Johny'
age = 55

print('hi ' + name + '. You are ' + str(age) + ' years old')
print(f'hi {name}. You are {age} years old')
```

## String indexes

```python
hello = 'hello'
print(hello[0]) #h
print(hello[4]) #o
print(hello[-1]) #o
print(hello[-5]) #h

# String slicing
# [start:stop:stepover]
# include start index
# exclude stop index
print(hello[0:2]) #01
print(hello[1:]) #ello
print(hello[0:5:2]) #hlo
print(hello[:2]) #he
print(hello[::1]) #hello

print(hello[::-1]) #olleh
```

## Immutability

String is immutable, it can not be changed

```python
name = "Hieu"
name = "Ha"

name[1] = 'i' #error
```

## Built-in Functions/Methods

### Built-in functions

```python
str()
len('hello') #5
int()
type()
```

[Built-in Functions &#8212; Python 3.9.0 documentation](https://docs.python.org/3/library/functions.html)

### String methods

```python
quote = 'to be or not to be'
quote.upper() #TO BE OR NOT TO BE
quote.capitalize() #To Be Or Not To Be    
quote.find('be') #3
quote.replace('be', 'me') #to me or not to me

# String is immutable
print(quote) #to be or not to be
```

## Booleans

```python
True #0
False #1
```

## Exercise Type Conversion

```python
birth_year = input('What year were you born? ')
birth_year = int(birth_year)
age = 2020 - birth_year
print(f'You are {age} years old.')
```