# Set:
Set is one of 4 built-in data types in Python used to store collections of data. It doesnot return repeated values.\
*Example 01* :
```python
a = {1,2,3,4,3,7,8,1,1} # set/unique
print(a)
```

Output:
```
{1, 2, 3, 4, 7, 8}
```
---

*Example 02* :
```python
a = {'c',1,2,3,3,3, 'a',20,'b','c'}
print(a)
```

Output:
```
{'c', 1, 2, 3, 20, 'a', 'b'}
```

*Example 03* :
```python
a={'d',4,33,'a','a'}
print(a)
```

Output:
```
{'d', 33, 4, 'a'}
```
=========================================================

* Set cannot update and its indexing is also not possible.

```python
a = {1,2,3,4,3,7,8,1,1}
print(a[0]) # indexing not allowed
```

Output:
```
Error
```

```python
a={'d',4,33,'a','a'}
print(a)
```
=========================================================

* Set cannnot perform opeartions, so we need to convert set into list to perform opeartions.

```python
course = ['AI',"AI","DS","DS"] # list
print(course, type(course))

course = set(course) # set converted
print(course, type(course))

course = list(course)
print(course, type(course)) # converted into list

course.reverse() # reverse order
print(course, type(course))
```

Output:
```
['AI', 'AI', 'DS', 'DS'] <class 'list'>
{'DS', 'AI'} <class 'set'>
['DS', 'AI'] <class 'list'>
['AI', 'DS'] <class 'list'>
```

## Quiz Question:
By using following list, returns a list in which result came first in alphabetical order and than in numeric value.\
a = [1,2,2,2,2,3, 'a','b','x'] 

```python
a = [1,2,2,2,2,3, 'a','b','x'] # list
a = set(a) # set/unique #convert into unique values
print(a, type(a)) #to check type of a

#convert into list for apply any function on it
a = list(a)# now again change in list
print(a, type(a)) #to check type of a

a_string = [i for i in a] # all element
print(a_string)

a_string = [i for i in a if isinstance(i,str)] # all string
a_string = sorted(a_string)
print(a_string)

a_intiger = [i for i in a if isinstance(i,int)] # all int
a_intiger = sorted(a_intiger)
print(a_intiger)

a = a_string + a_intiger
print(a)
```

Output:
```
{1, 2, 3, 'x', 'a', 'b'} <class 'set'>
[1, 2, 3, 'x', 'a', 'b'] <class 'list'>
[1, 2, 3, 'x', 'a', 'b']
['a', 'b', 'x']
[1, 2, 3]
['a', 'b', 'x', 1, 2, 3]
```