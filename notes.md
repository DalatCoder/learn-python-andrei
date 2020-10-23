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

x,y,z *other = my_tuple

#2 methods on tuple
print(my_tuple.count(5)) #1
print(my_tuple.index(5)) #4
print(len(my_tuple)) #5
```

## Set

- Unordered collection of unique objects

```python
my_set = {1,2,3,4,5}
print(my_set) #{1,2,3,4,5}

my_set = {1,2,3,4,5,5}
print(my_set) #{1,2,3,4,5}

my_set.add(100);
my_set.add(2)
print(my_set) #{1,2,3,4,5,100}
```

- Get a set of unique number in a list

```python
my_list = [1,2,3,4,5,5]
my_set = set(my_list)
print(my_set) #{1,2,3,4,5}
```

- Set object does not support indexing

```python
my_set = {1,2,3,4,5}
my_set[0] #error
print(1 in my_set) #True
print(len(my_set)) #5

new_set = my_set.copy()

print(list(my_set)) #[1,2,3,4,5]
```

### Set methods (Venn diagram)

- difference()

- discard()

- difference_update()

- intersection()

- isdisjoint()

- issubset()

- issuperset()

- union()

```python
my_set = {1,2,3,4,5}
your_set = {4,5,6,7,8,9,10}

my_set.difference(your_set) #{1,2,3}
my_set.discard(5) #{1,2,3,4}
my_set.difference_update(your_set) #{1,2,3}
my_set.intersection(your_set) #{4,5}
my_set.isdisjoint(your_set) #False
my_set.union(your_set) #{1,2,3,4,5,6,7,8,9,10}

# union
print(my_set | your_set)

# intersection
print(my_set & your_set)

my_set = {4,5}
my_set.issubset(your_set) #True
your_set.issuperset(my_set) #True
```

## Conditional Logic

```python
is_old = True
is_licenced = True

if is_old:
    print('You are old enough to drive!')
elif is_licenced:
    print('You can drive now!')
else:
    print('You are too young!')
print('Out side if code block')
```

- Use expression

```python
is_old = True
is_licenced = True

if is_old and is_licenced:
    print('Drive drive')
```

### Indentation in Python

Be careful with spaces

### Truthy and Falsy

```python
bool('hello') #True
bool(5) #True

bool('') #False
bool(0) #False
bool(None)

password = '123'
username = 'hieu'

if password and username:
    print('Login!')
```

### Ternary Operator

<mark>condition_if_true **if** condition **else** condition_if_false</mark>

```python
is_friend = True
can_message = "message allowed" if is_friend else "not allowed to message"

print(can_message)
```

### Short Circuiting

```python
is_friend = True
is_user = True

print(is_friend and is_user) #True
print(is_friend or is_user) #True
```

- Trong mệnh đề and
  
  - Nếu is_friend = false thì không cần kiểm tra vế sau nữa

- Trong mệnh đề or
  
  - Nếu is_friend = true thì không cần kiểm tra vế sau nữa

=> Short circuiting

### Logical Operators

```python
4 > 5 #False
4 < 5 #True
4 == 4 #True
4 != 4 #False
1 <= 2 <= 3 #True
1 < 2 > 3 < 4 #False short circuiting
and
or
not
```

### Is

```python
print(True == 1) #True
print('' == 1) #False
print('1' == 1) #False
print([] == 1) #False
print(10 == 10.0) #True
print([] == []) #True
```

- == convert 2 operand to the same type

- == Check for the equality of value (auto type conversion)

```python
print(True is 1) #False
print('1' is 1) #False
print([] is 1) #False
print(10 is 10.0) #False
print([] is []) #False

print(True is True) #True
print('1' is '1') #True
print([] is []) #False
print(10 is 10) #True
print([1,2,3] is [1,2,3]) #False
```

- is check for the address in memory

### Loops

Iterable: Something we can loop over:

- 'This is a string'

- [1,2,3,4,5]

#### For loop

```python
for letter in 'Zero to Mastery':
    print(letter)
print('Finish')
print(letter) #y
```

### Iterable

A collection that can be iterated over

- list

- dictionary

- tuple

- set

- string

#iterate -> one by one check each item in the collection.

```python
# Iterate over a dictionary
user = {
    'name': 'Golem',
    'age': 5006,
    'can_swim': False
}

for item in user:
    print(item)
# Key

for item in user.items():
    print(item)
# Tuple

for key, value in user.items():
    print(key, value)

for item in user.values():
    print(item)
# Value

for item in user.keys():
    print(item)
# Key
```

### Range()

```python
print(range(100)) #range(0, 100) | range #0object
print(range(0, 100)) #range(0, 100)

for number in range(0, 100):
    print(number)

#0 - #99: Loop 100 times

for _ in range(0, 10):
    print('Hello')

for _ in range(0, 10, 2):
    print(_)
# 0 2 4 6 8

for _ in range(10, 0, -1):
    print(_1)
# 10 9 8 7 6 5 4 3 2 1

```

#### Quick way to create a list which have integers

```python
# Quick way to create a list which have integers
for _ in range(2):
    print(list(range(10)))
```

### Enumerate() | Access index number

```python
for idx, char in enumerate('Hello'):
    print(idx, char)
```

```python
for i, number in enumerate(list(range(100))):
    if number == 50:
        print(f'The index of 50 is: {i}')
        break
```

### While loop

while condition:

    do_something

```python
i = 0
while i < 50:
    print(i)
    i += 1
# Special key
else:
    print('done with all the work')
```

The else block will only execute if there is no break statement

```python
i = 0
while i < 10:
    print(i)
    i += 1
    break
else:
    print('Else block never be executed') 
```

## What is good code?

- Clean (following best practices)

- Readability

- Predictability

- DRY: Don't repeat yourself