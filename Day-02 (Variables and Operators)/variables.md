# Variables
Variables- changes time to times (it varies)
E.g. Login system - Same interface but different data.

There are two types of applications:
1. Static application - It changes the whole system for everyone (changes by programmer)
E.g. A backend developer changes the software (means hardcore changes) - Like if 'Facebook' name changes to 'Meta'
2. Dynamic application - It changes by the user 
E.g. A login page - in which every user has different 'name, pic etc'

There are two types of variables:
1. Static Variable
2. Dynamic Variable


<span style="color: lightblue;">**Example**</span> 
```python
name = "Hafsa Imtiaz"
print(name)
print (type(name)) #type tells class data type
print (id(name))  #id tells memory address - i.e. physical address of varaible
```

Output:
``` markup
Hafsa Imtiaz
<class 'str'>
2109776480048
```

## Data Types:
Python has five standard data types:
* Number data type - Integar, Float, Complex
* Text data type - String
* List
* Tuple
* Dictionary

<span style="color: lightblue;">**Example # 1**</span> 
```python
a = 20   #integar
print(a, type(a), id(a))

b = 20.7  #float
print(b, type(b), id(b))

c = [1, 2, 3]    #list
print(c, type(c), id(c))

d = {1, 1, 1, 2, 5, 5, 2}  # set(it return only unique values)
print(d, type(d), id(d))

e = {"name": "Hafsa", "education": "NED"} # dictionary
print(e, type(e), id(e))
```

Output:
```markup
20 <class 'int'> 140717744711048
20.7 <class 'float'> 2365709794832
[1, 2, 3] <class 'list'> 2365710682624
{1, 2, 5} <class 'set'> 2365712095424
{'name': 'Hafsa', 'education': 'NED'} <class 'dict'> 2365712083456
```

<span style="color: lightblue;">**Example # 2**</span> 
Dynamic Data Type
```python
a = 7
print(a, type(a), id(a))
b = '7'
print(b, type(b), id(b))
c = 7.0
print(c, type(c), id(c))
```

Output:
```markup 
7 <class 'int'> 140717744710632
7 <class 'str'> 140717744754128
7.0 <class 'float'> 1472384769552
```

## Shallow Copy & Deep Copy
* Shallow copy - same data - means same physical address but different name
* Deep copy - means different physical address as well as different name

<span style="color: lightblue;">**Example**</span> - Shallow Copy
```python
x = 6
y = 6
z = 6
print(id(x))
print(id(y))
print(id(z)) # as these stoe data in memory - it is "Shallow copy"
```

Output:
```markup
140717644833736
140717644833736
140717644833736
```
<span style="color: lightblue;">**Example**</span> - Deep Copy
```python
a = 7
b = '7'
print(id(a))
print(id(b))
```

Output:
```markup
140717644833768
140717644877264
```

## Note
* Java - is restricted data type
* In java we write - type variableName = value
* While Python - is dynamic data type.
* In python we write - variable_name = value
* According to PP8 standard - there should be space before and after operator.
* type function - tells about 'class'
* id - tells the 'memory address' - i.e. block address. 