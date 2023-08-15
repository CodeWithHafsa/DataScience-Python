# List Methods:
Python has a set of built-in methods that can use on lists/arrays.


|S.No.| Method        |  Description           |
|----|-------------------|----------------------------------|
|1.|  append()| Adds an element at the end of the list      | 
|2.|  clear()|  Removes all the elements from the list      | 
|3.|  copy()|   Returns a copy of the list      | 
|4.|  count()|  Returns the number of elements with the specified value      | 
|5.|  extend()|  Add the elements of a list (or any iterable), to the end of the current list      | 
|6.|  index()|  Returns the index of the first element with the specified value      | 
|7.|  insert()| Adds an element at the specified position      | 
|8.|  pop()| Removes the element at the specified position      | 
|9.|  remove()| Removes the first item with the specified value      | 
|10.|  reverse()| Reverses the order of the list    | 
|11.|  sort()| Sorts the list    | 

## Methods of List:

*Example* :
```python
a = list(range(1,11))
[i for i in dir(a) if "_" not in i]
```

Output:
```
['append',
 'clear',
 'copy',
 'count',
 'extend',
 'index',
 'insert',
 'pop',
 'remove',
 'reverse',
 'sort']
```

## 1. append():
This method adds an element at the end of the list.

*Example* :
```python
names = []
print(names)
names.append("Qasim")
print(names)
names.append("Asif")
print(names)
names.append("Hamza")
print(names)
```

Output:
```
[]
['Qasim']
['Qasim', 'Asif']
['Qasim', 'Asif', 'Hamza']
```

*Example* :
```python
names = ['Qasim', 'Asif', 'Hamza']
while True:
    name1 = input("Enter Student Name | X for exit")
    if name1 == "X" or name1 =="x":
        break
    names.append(name1)

names
```

Output:
```
Enter Student Name | X for exitUbaid
Enter Student Name | X for exitkonain
Enter Student Name | X for exitIbad
Enter Student Name | X for exitx
['Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
```
## 2. clear():
This method removes all the elements from a list.

*Example* :
```python
fruits = ["apple", "banana", "cherry"]
fruits.clear()
print(fruits)
```

Output:
```
[]
```

## 3. copy():
This method returns a copy of the list. This can be done to perform operations on the list without modifying the original list.

* *Example: Shallow copy*
---> Changes occur in both old and new list.

```python
names = ['Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
st_names = names # shallow copy
st_names
st_names[0] #index

st_names[0] = "Muhammad Qasim"
print(st_names) #change occur in both lists
print(names)
```

Output:
```
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
```
---
* *Example: Using copy() function* ---> Changes occur ony in new list, while old list remains same.

```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
st_names1 = names.copy() # deep copy
st_names1

st_names1[0] = "Qasim"
print(names) 
print(st_names1) #change occur only in new list
```

Output:
```
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
['Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
```
---
* *Example: Using Slicing / Indexing* ---> Changes occur ony in new list, while old list remains same.

```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
print(names)
n = names[:] # deep copy
n[0] = 'Qasim1'

print(names)
print(n) #change occur only in new list
```

Output:
```
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
['Qasim1', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
```

## 4. count():
Returns the number of elements with the specified value.

*Example*
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
names.count("Asif")
```

Output:
```
1
```

## 5. extend():
This method adds an entire list or any other collection datatype (set, tuple, dictionary) to the existing list.

*Example: Append* :
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
names.append('111')
names.append('222')
names.append(['333'])
print(names)
```

Output:
```
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad', '111', '222', ['333']]
```

*Example: Extend*
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad', '111', '222', ['333']]
remaining_names = ['a','b','c']
names.extend(remaining_names)
print(names)
```

Output:
```
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad', '111', '222', ['333'], 'a', 'b', 'c']
```

*Example: To delete a string*
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad', '111', '222', ['333'], 'a', 'b', 'c']
del names[-4]
print(names)
```

Output:
```
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad', '111', '222', 'a', 'b', 'c']
```

## 6. index():
Returns the index of the first element with the list item.

*Example* :
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad', '111', '222', 'a', 'b', 'c']
names.index("Konain")
```

Output:
```
4
```

## 7. insert():
This method adds an element at the specified position.

*Example* :
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
names.insert(0,"Eman")
print(names)
```

Output:
```
['Eman', 'Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
```

## 8. pop():
This method removes the element at the specified position.

*Example* :
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
c  = names.pop()
print(c)
print(names)
```

Output:
```
Ibad
['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain']
```

## 9. remove():
This method removes the first item with the specified value.

*Example* :
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
names.remove("Ubaid")
print(names)
```

Output:
```
['Muhammad Qasim', 'Asif', 'Hamza', 'Konain', 'Ibad']
```

## 10. reverse():
This method reverses the order of the list. 

*Example* :
```python
names = ['Muhammad Qasim', 'Asif', 'Hamza', 'Ubaid', 'Konain', 'Ibad']
names.reverse()
print(names)
```

Output:
```
['Ibad', 'Konain', 'Ubaid', 'Hamza', 'Asif', 'Muhammad Qasim']
```

## 11. sort():
This method sorts the list in ascending order. The original list is updated.

*Example 1* :
```python
l = [11, 45, 1, 2, 4, 6]
print(l)
l.sort() #sort in ascending order
print(l)
```

Output:
```
[1, 2, 4, 6]
[1, 2, 4, 6]
```
---
*Example 2* :
```python
cars = ['Ford', 'BMW', 'Volvo']
cars.sort()
print(cars)
```

Output:
```
['BMW', 'Ford', 'Volvo']
```
---
* For descending order give ---> reverse=True

*Example 1* :
```python
l = [11, 45, 1, 2, 4, 6]
print(l)
l.sort(reverse=True) #sort in descending order
print(l)
```

Output:
```
[1, 2, 4, 6]
[6, 4, 2, 1]
```

*Example 2* :
```python
cars = ['Ford', 'BMW', 'Volvo']
cars.sort(reverse=True)
print(cars)
```

Output:
```
['Volvo', 'Ford', 'BMW']
```
