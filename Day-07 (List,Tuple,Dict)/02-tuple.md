### Inbuilt Data Types:
* List
* Tuple
* Dictionary
* Set

---

**CREATION TIME:**

* create **list** [elem1,elem2,...] - Starts and ends with square bracket **[ ]**
* create **tuple** (elem1,elem2,...) - Starts and ends with round bracket **( )**
* create **dictionary** {key:value, key2:value2,...} - Starts and ends with curly bracket **{ }**
* create **set** { elem1,elem2,... } - Starts and ends with curly bracket **{ }**

**CALLING TIME:**
* list_var[index] - Starts and ends with square bracket **[ ]**
* tup_var[inde] - Starts and ends with square bracket **[ ]**
* dict_var[key] - Starts and ends with square bracket **[ ]**

# List:
Lists are used to store multiple items in a single variable.

### *Example: To update a string using index number*:
Only List are mutable - means it can change/upadate. While, tuple, string, dictionary are immutable.

```python
#        0                1             2  index
a = ['Muhammad Aslam',"Muhammad Qasim",30] # value,element
a[1] #calling using index number
```

Output:
```
'Muhammad Qasim'
```
========================================================

* In below example - 'Muhammad Qasim' update with 'Qasim'

```python
a[1] = 'Qasim' #update/calling
print(a)
```

Output:
```
['Muhammad Aslam', 'Qasim', 30]
```
========================================================

* Below is a example of string - it can't update, because strings are immutable. 

```python
a = 'Muhammad Qasim'
print(a)
a[0] = 'm' #string cannot update
print(a) 
```

Ouput:
```
Error
```

# Tuple:
Tuples are used to store multiple items in a single variable. Tuples are immutable. 

* *Example: Print Tuple*
```python
#     0   1   2
a = ('X','Y','Z')
#.   -3  -2  -1
print(a) 
```

Output:
```
('X', 'Y', 'Z')
```
========================================================

* *Example: Print Tuple using loop*
```python
a = ('X','Y','Z')
for i in a:
    print(i)
#a[0] #positive index (ans='X')
#a[-1] #negative index (ans='Z')
```

Output:
```
X
Y
Z
```
========================================================

* Tuples aree immutable, means it cannot update.
```python
a[0] = "Pakistan" #Tuple cannot update
print(a)
```

Ouput:
```
Error
```
========================================================

* If we want to change tuple, we have to create a new tuple, means we have to re-assign the value.
```python
#     0  1  2
a = ('X','Y','Z')
#.   -3  -2 -1
print(a)
print(id(a))

a = ('Pakistan','Y',"Z") # re-assign we change whole variable
print(a)
print(id(a))
```

Output:
```
('X', 'Y', 'Z')
2135820734976
('Pakistan', 'Y', 'Z')
2135819576384
```
========================================================

* To know the 'Tuple methods ( ) - use dir function':
```python
a = ('Pakistan','Y',"Z") 
[i for i in dir(a) if "__" not in i]
```

Output:
```
['count', 'index']
```

# Tuple Methods:
## 1. count():
The count() method - Returns the number of times a specified value appears in the tuple.

```python
thistuple = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
x = thistuple.count(5)
print(x)
```

Output:
```
2
```

## 2. index():
The index() method finds the first occurrence of the specified value.\
The index() method raises an exception if the value is not found.

```python
thistuple = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
x = thistuple.index(8)
print(x)
```

Output:
```
3
```

## Key Point:
* **hashable functions** - hashable is a feature of Python objects that tells if the object has a hash value or not. If the object has a hash value then it can be used as a key for a dictionary or as an element in a set. \
These are public or private key.
* **List** are mutable - means it is changable.
* **Tuple** are immutable - means it does not change.
* **string** are immutable - means it does not change.
* **blockchain** are immutable - means it does not change.