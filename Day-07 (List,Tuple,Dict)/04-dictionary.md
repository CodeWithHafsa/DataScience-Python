# Dictionary:
Dictionaries are mutable data structures that allow you to store key-value pairs.

### Syntax: Now replace index number with Key:

```
{
    key1 : value1,
    key2 : value2,
}

* key = str, int
* value = str, int, float, list, tuple, dict...
```
========================================================

* *Example 01*:
```python
a = {
    'fname':'Muhammad Aslam', 
     'name':"Muhammad Qasim",
     'age':30
    } 

print(a) 
a['name']
```

Output:
```
{'fname': 'Muhammad Aslam', 'name': 'Muhammad Qasim', 'age': 30}
'Muhammad Qasim'
```
========================================================

* *Example 02*:
```python
d = {
    'a':"Pakistan", #key:string
    20: "Hello world" #key:list
    #(1,2,3): "ABCD" #key:tuple - wrong method
    }
print(d)
print(d[20]) #here 20 is key value
print(d['a'])
```

Output:
```
{'a': 'Pakistan', 20: 'Hello world'}
Hello world
Pakistan
```
========================================================

* *Example 03: Indexing in dictionary*:
```python
data = {"roll_no": [1, 2, 3, 4]}
print(data) #dictionary
print(data['roll_no']) #list
print(data ['roll_no'][2]) #integar
```

Output:
```
{'roll_no': [1, 2, 3, 4]}
[1, 2, 3, 4]
3
```
========================================================

* *Example 04: Indexing in dictionary*:

```python
#    0  1  2              3
a = [1, 2, 3, {'d': '1', 'name': 'Ali'}] #integar and dictionary
print(a)
print(a[-1]) #indexing
print(a[-1]['name']) #indexing #here name is key
```

Output:
```
[1, 2, 3, {'d': '1', 'name': 'Ali'}]
{'d': '1', 'name': 'Ali'} #dictionary
Ali 
```

## Use of isinstance:
The isinstance() function returns True if the specified object is of the specified type, otherwise False.

*Example 01*:
```python
#    0  1  2              3
a = [1, 2, 3, {'d': '1', 'name': 'Ali'}] #integar and dictionary
print(a)
print(type(a))
isinstance(a, list) # match one data type with your datatype
```

Output:
```
[1, 2, 3, {'d': '1', 'name': 'Ali'}]
<class 'list'>
True
```
=====================================================

*Example 02*:
```python
i = [1,23]

print(isinstance(i,str))
print(isinstance(i,list))
print(isinstance(i,tuple))
print(isinstance(i,set))
print(isinstance(i,dict))
print(isinstance(i,float))
print(isinstance(i,bool))
print(isinstance(i,int))
print(isinstance(i,complex))
```

Output:
```
False
True
False
False
False
False
False
False
False
```
=====================================================

*Example 03*:
```python
i = "Python"
print(isinstance(i,str))
```

Output:
```
True
```