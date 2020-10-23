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

## Python best practices

[Python best practices](https://realpython.com/)

## Exercise Password Checker

```python
username = input('Enter your username: ')
password = input('Enter your password: ')
password_length = len(password)
password_hidden = '*' * password_length

message = f'''
Username: {username}
Password: {password_hidden}
Password length: {password_length}
'''

print(message)
```

## Data Structure

### 1. List (Order sequence of object)[Array like]

```python
li = [1, 2, 3, 4, 5]
li2 = ['a', 'b', 'c']
li3 = [1, 2, 'a', 'b', True]

amazon_cart = ['notebooks', 'sunglasses']
amazon_cart[0] #notebooks
amazon_cart[1] #sunglasses
amazon_cart[2] #error: list index out of range
```

#### List slicing

```python
# [start:stop:step]
amazon_cart = [
    'notebooks',
    'sunglasses',
    'toys',
    'grapes'
]

print(amazon_cart[0:2]) #notebooks, sunglasses
print(amazon_cart[0::2]) #notebooks, toys
```

#### List is mutable

```python
amazon_cart = [
    'notebooks',
    'sunglasses',
    'toys',
    'grapes'
]

amazon_cart[0] = 'laptop'

new_cart = amazon_cart[0:3]
# new_cart ['laptop', 'sunglasses']
# amazon_cart ['laptop', 'sunglasses', 'toys', 'grapes']
```

#### Copy a list

```python
amazon_cart = [
    'notebooks',
    'sunglasses',
    'toys',
    'grapes'
]

new_cart = amazon_cart[:]

# Don't do that
new_cart = amazon_cart
```

#### List methods

```python
basket = [1, 2, 3, 4, 5]
len(basket) #5

# adding
basket.append(6) #[1, 2, 3, 4, 5, 6]

# insert
basket.insert(0, 0) #[0, 1, 2, 3, 4, 5, 6]

# extend
basket.extend([7, 8]) #[0, 1, 2, 3, 4, 5, 6, 7, 8]

# removing
basket.pop() #8
print(basket) #[0, 1, 2, 3, 4, 5, 6, 7]

basket.pop(0) #0
print(basket) #[1, 2, 3, 4, 5, 6, 7]

basket.remove(7) #None
print(basket) #[1, 2, 3, 4, 5, 6]

basket.clear() #None
print(basket) #[]

basket = ['a', 'b', 'c', 'd', 'e']

# indexOf
basket.index('d') #3
# Error if not found

print('d' in basket) #True
print('x' in basket) #False
print(basket.count('d')) #1

basket.sort() #None
print(basket) #['a', 'b', 'c', 'd', 'e']

sorted(basket) #['a', 'b', 'c', 'd', 'e']

basket.reverse() #None
print(basket) #['e', 'd', 'c', 'b', 'a']
```

#### Common list patterns

```python
basket = ['a', 'b', 'c', 'd', 'e']

# reverse
print(basket[::-1])

# copy a list
print(basket[:])

# range
print(list(range(1, 100)))

# join
sentence = ' '.join(['hi', 'my', 'name', 'is', 'JOJO'])

print(sentence) #hi my name is JOJO
```

#### List unpacking

```python
a,b,c, *other, d = [1,2,3,4,5,7,8,9]

print(a) #1
print(b) #2
print(c) #3
print(other) #[4,5,6,7,8]
print(d) #9
```

### Matrix

Come up a lot in machine learning and image processing

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

photo = [
    [1, 0, 1],
    [0, 1, 0],
    [1, 0, 1]
]
#print X

matrix[0] #[1,0,1]
matrix[0][1] #2
```

## None (null like, represent the absent of value)

## Dictionary (hash table | Data type | Data structure)

```python
# unorder key:value pairs
dictionary = {
    'a': [1,2,3],
    'b': 'Hello',
    'x': True
}

print(dictionary['a'][1]) #1
print(dictionary['b']) #'Hello'
print(dictionary['c']) #error

my_list = [
    {
        'a': [1,2,3],
        'b': 'Hello',
        'x': True
    },
    {
        'a': [1,2,3],
        'b': 'Goodbye',
        'x': False
    }        
]

my_list[0]['a'][1] #1
```

## Understanding Data Structures

Hiểu và xác định được khi nào nên dùng data structure nào:

- List

- Dictionary

### Dictionary keys

```python
dictionary = {
    123: [1,2,3],
    True: 'hello',
    'key': 'word'
}
```

- The key must be immutable

- The key have to be unique

### Dictionary methods

```python
user = {
    'basket': [1,2,3],
    'greet': 'hello'
}

print(user.get('age')) #None

# Get age from user dictionary
# If age doesn't exist, use 44, (default value)
print(user.get('age', 44)) #44

# Check if key exists in dict
print('basket' in user) #True
print('size' in user) #False

# Get list of keys
user.keys();

# Get list of values
user.values();

# Entire item (key:value pairs | tuple)
user.items();

# Clear
user.clear() #None
print(user) #{}

# Copy
user_copied = user.copy()

# Pop | Remove key
print(user.pop('basket')) #[1,2,3]

# PopItem
print(user.popitem) # Randomly pop item

# Update
user.update({'greet': 'goodbye world!'})

# Another way to create dictionary
user2 = dict(name='JohnJohn')
print(user2)
```

## Tuple

- List like, but immutable

- If the list don't expect to be changed, use tuple

```python
my_tuple = (1,2,3,4,5)
my_tuple[1] = 0 #error

print(my_tuple[1]) #2
print(5 in my_tuple) #True
```