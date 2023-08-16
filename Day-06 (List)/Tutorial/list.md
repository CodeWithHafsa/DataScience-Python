# Slicing
A slice object is used to specify how to slice a sequence. Slicing can be: Positive or Negative.

It is used to return a particular range value.

Syntax: ```list_variable[start:end:step]```
* start = this number will be included
* end = this number will be excluded - i.e. end-1
* step = sequence/gap
  * step = 1 (positive value - means left to right) #it is by-default
  * step = -1 (negative value - means right to left) 

---

* *Example: List*
```python
characters = list("abcdefghijklmnopqrstuvwxyz") #list function used to convert string into list
print(characters)
```

Output:
```
['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
```
---

* *Example: Loop*
```python
characters = "abcdefghijklmnopqrstuvwxyz"

counter = 0
while (Counter < len(characters))
   print(characters[counter]) #generate infinite loop
   counter +=1  #update one character until all characters ends
   #or counter +=2  #update two character until all characters ends
```

---
## Positive and Negative Slicing
* Positive slicing - goes from left to right (bydefault). For this, step = 1
* Negative slicing - goes from right to left. For this, step = -1.

* *Example#1: Indexing and Slicing*
```python
a = (list(range(1,11)))
print(a)
print(a[0])   #indexing

print(a[1:2]) #slicing
print(a[1:7]) #slicing
```

Output:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
1

[2]
[2, 3, 4, 5, 6, 7]
```

*Example#2: Slicing*
```python
a = (list(range(1,11)))
print(a[::]) #if nothing is written - means all value include
print(a[0:10:1]) #Here: start=0, end=10, step-1
print(a[0:10:2]) 
print(a[0:10:3]) 
```

How it works:
```python
#positive - from right to left
#  0  1  2  3  4  5  6  7  8   9 ---> positive  
    "1,  2,  3,  4,  5,  6,  7,  8,  9,  10"
#  -10  -9  -8  -7  -6  -5  -4  -3  -2   -1 <--- negative 
#negative - from left to right
```

Output:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
[1, 3, 5, 7, 9]
[1, 4, 7, 10]
```

* All got same result:

*Example#2: Slicing from left to right*
```python
a = (list(range(1,11)))
print(a[3::]) 
print(a[3:]) 
print(a[3:10]) 
print(a[3:10:1]) 
print(a[-7:]) #negative slicing
```

Output:
```
[4, 5, 6, 7, 8, 9, 10]
[4, 5, 6, 7, 8, 9, 10]
[4, 5, 6, 7, 8, 9, 10]
[4, 5, 6, 7, 8, 9, 10]
[4, 5, 6, 7, 8, 9, 10]
```

* When start is greater than end, and step=1 (positive) - then result is empty set. To resolve it, start should be greater than end. 

*Example#3: Slicing empty set*
```python
a = (list(range(1,11)))
print(a[-2:-5]) #empty result - because by default step is '1'
print(a[-5:-2])
```

Output:
```
[]
[6, 7, 8]
```

*Example: Slicing from right to left*
```python
a = (list(range(1,11)))
print(a)
print(a[::-1])
print(a[-2:-5:-1]) #from right to left, because step =-1
```

Output:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
[9, 8, 7]
```

## Key Points:
* Lazy Evaluation using Python:  It saves the execution time for larger ranges and we never require all the values at a time, so it saves memory consumption as well
* Generative function - It allows you to declare a function that behaves like an iterator, providing a faster and easier way to create iterators. E.g.lists, dictionaries, strings, range function. (means it returns as it is value).

* *Example:* &nbsp; ```a = (list(range(1,11)))```

   *Result*:  &nbsp; ```range(1,11)```