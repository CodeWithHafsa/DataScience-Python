# Data Types in Python:
Data types specify the type of data that can be stored inside a variable.

|   Data Types             |Classes                          |Description                         |
|----------------|-------------------------------|-----------------------------|
|Numeric|`int, float, complex`            | holds numeric values             |
|String|`str`            | holds sequence of characters             |
|Sequence|`list, tuple, range`            | holds collection of items             |
|Mapping|`dict`            | holds data in key-value pair form             |
|Boolean|`bool`            | holds either True or False             |
|Set|`set, frozeenset`            | hold collection of unique items             |
|Binary|`bytes, bytearray, memoryview`            | includes bytes, bytearray, and memoryview             |
|None|`NoneType`            | represents the absence of a value             |

## 1. Python Numeric Data type:
In Python, numeric data type is used to hold numeric values.
* ```int``` - It contains positive or negative whole numbers.
* ```float``` - It is a real number with a floating-point representation. It is specified by a decimal point.
* ```complex``` - holds complex numbers. It is specified as (real part) + (imaginary part)j. For example – 2+3j

*Example*
```python
a = 5
print(a, 'is of type', type(a))

b = 2.0
print(b, 'is of type', type(b))

c = 1+2j
print(c, 'is of type', type(c))
```

Output:
```
5 is of type <class 'int'>
2.0 is of type <class 'float'>
(1+2j) is of type <class 'complex'>
```

## 2. Python String Data Type:
A string ```str``` is a collection of one or more characters put in a single quote, double-quote, or triple-quote. 

*Example*
```python
String1 = 'Welcome to the Geeks World' # Single Quote String
print("String with the use of Single Quotes: ")
print(String1)
 
String1 = "I'm a Geek"   # Double Quote String
print("\nString with the use of Double Quotes: ")
print(String1)
print(type(String1))
 
String1 = '''I'm a Geek and I live in a world of "Geeks"''' # Triple Quote String
print("\nString with the use of Triple Quotes: ")
print(String1)
print(type(String1))
```

Output:
```
String with the use of Single Quotes: 
Welcome to the Geeks World

String with the use of Double Quotes: 
I'm a Geek
<class 'str'>

String with the use of Triple Quotes: 
I'm a Geek and I live in a world of "Geeks"
<class 'str'>
```

## 3. Python Sequence Data Type:
The sequence Data Type in Python is the ordered collection of similar or different data types. It includes - List, Tuple, Range.

* ```list``` - List is an ordered collection of similar or different types of items separated by commas and enclosed within brackets ```[ ]```.

*Example*
```python
x = ["apple", "banana", "cherry"]
print(x)
print(type(x)) 
```

Ouput:
```
['apple', 'banana', 'cherry']
<class 'list'>
```

* ```Tuple``` - Tuple is an ordered sequence of items same as a list. The only difference is that tuples are immutable. Tuples once created cannot be modified.

*Example*
```python
x = ("apple", "banana", "cherry")
print(x)
print(type(x)) 
```

Output:
```
('apple', 'banana', 'cherry')
<class 'tuple'>
```

* ```Range``` - Python range is a function that returns a sequence of numbers.

*Example*
```python
x = range(6)
print(x)
print(type(x)) 
```

Output:
```
range(0, 6)
<class 'range'>
```

## 4. Python Mapping Data Type:
A mapping type is a data type comprised of a collection of keys and associated values. The mapping in Python is the dictionary, which allows you to store key-value pairs.

* ```Dict``` - Python's only built-in mapping type is the dictionary.

*Example*
```python
x = {"name" : "John", "age" : 36}
print(x)
print(type(x)) 
```

Output:
```
{'name': 'John', 'age': 36}
<class 'dict'>
```

## 5. Python Boolean Data Type:
The boolean ```bool``` in Python represents logical values True and False.

*Example*
```python
x = True
print(x)
print(type(x)) 
```

Output:
```
True
<class 'bool'>
```

## 6. Python Set Data Type:
The set and frozenset in Python allow you to store a collection of unique items.

* ```set``` - In Python, a Set is an unordered collection of data types that is iterable, mutable and has no duplicate elements. 

*Example*
```python
x = {"apple", "banana", "cherry"}
print(x)
print(type(x)) 
```

Output:
```
{'banana', 'cherry', 'apple'}
<class 'set'>
```

* ```frozenset``` - Frozen set is just an immutable version of a Python set object. While elements of a set can be modified at any time, elements of the frozen set remain the same after creation.

*Example*
```python
x = frozenset({"apple", "banana", "cherry"})
print(x)
print(type(x)) 
```

Output:
```
frozenset({'banana', 'cherry', 'apple'})
<class 'frozenset'>
```

## 7. Python Binary Data Type:
Binary in Python includes bytes, bytearray, and memoryview.

* ```Byte``` - The byte data type in Python is used to represent a group of 8 binary digits. It is a built-in data type. 

A byte in Python can hold any value from 0 to 255. It is typically used to represent binary data, such as images or audio files, or to work with low-level network protocols.

*Example*
```python
x = b"Hello"
print(x)
print(type(x)) 
```

Output:
```
b'Hello'
<class 'bytes'>
```

* ```Byte``` - The bytearray data type in Python is a mutable sequence of bytes. It is a built-in data type.

*Example*
```python
x = bytearray(5)
print(x)
print(type(x)) 
```

Output:
```
bytearray(b'\x00\x00\x00\x00\x00')
<class 'bytearray'>
```

* ```Memory View``` - Memory View allows you to view the memory of an object without creating a copy of it, making it useful for working with large data sets.

*Example*
```python
x = memoryview(bytes(5))
print(x)
print(type(x)) 
```

Output:
```
<memory at 0x013D8FA0>
<class 'memoryview'>
```

## 8. Python None Data Type:
The NoneType data type represents the absence of a value.  It is a built-in type that has only one value: None.

*Example*
```python
x = None
print(x)
print(type(x)) 
```

Output:
```
None
<class 'NoneType'>
```