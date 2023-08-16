# Extra Code - For Numpy:

* Nested list - means list within a list
* Dimensions count: Jitney opening ya closing brackets hongey utni dimension hogi.
* e.g. In below example there are 2 opening or closing brackets - it means it has 2 dimensions. 
* List limitation - it cannot do multiline slicing, that's why we have to use numpy array or otherwise use comprehensive method.

*Generate counting in list using numpy*
```python
import numpy as np #nested list

a = np.arange(1,101).reshape(10,10).tolist()
print(a)
```

Output:
```
[[1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 
[11, 12, 13, 14, 15, 16, 17, 18, 19, 20], 
[21, 22, 23, 24, 25, 26, 27, 28, 29, 30], 
[31, 32, 33, 34, 35, 36, 37, 38, 39, 40], 
[41, 42, 43, 44, 45, 46, 47, 48, 49, 50], 
[51, 52, 53, 54, 55, 56, 57, 58, 59, 60], 
[61, 62, 63, 64, 65, 66, 67, 68, 69, 70], 
[71, 72, 73, 74, 75, 76, 77, 78, 79, 80], 
[81, 82, 83, 84, 85, 86, 87, 88, 89, 90], 
[91, 92, 93, 94, 95, 96, 97, 98, 99, 100]]
```

* To display list as it is - use ```display``` function

```python
display(a)
```

Output:
```
[[1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 
[11, 12, 13, 14, 15, 16, 17, 18, 19, 20], 
[21, 22, 23, 24, 25, 26, 27, 28, 29, 30], 
[31, 32, 33, 34, 35, 36, 37, 38, 39, 40], 
[41, 42, 43, 44, 45, 46, 47, 48, 49, 50], 
[51, 52, 53, 54, 55, 56, 57, 58, 59, 60], 
[61, 62, 63, 64, 65, 66, 67, 68, 69, 70], 
[71, 72, 73, 74, 75, 76, 77, 78, 79, 80], 
[81, 82, 83, 84, 85, 86, 87, 88, 89, 90], 
[91, 92, 93, 94, 95, 96, 97, 98, 99, 100]]
```

*To generate comprehensive list*
```python
[i [5:8] for i in a ] #it collects 5to7 numbers from every list.
```

Output:
```
[[6, 7, 8],
 [16, 17, 18],
 [26, 27, 28],
 [36, 37, 38],
 [46, 47, 48],
 [56, 57, 58],
 [66, 67, 68],
 [76, 77, 78],
 [86, 87, 88],
 [96, 97, 98]]
```

# Comprehension Method for 'for loop':
We can create new sequences using a given python sequence. This is called comprehension. It basically a way of writing a concise code block to generate a sequence which can be a list, dictionary, set or a generator by using another sequence.
(means a style to write a code in one line)

* list, tuple, strings - are iterative data types.

*Example: string iterative data type*
```python
for i in "abcdef":
    print(i) #i means iteration #loop
```

Output:
```
a
b
c
d
e
f
```
---
*Example: string iterative data type*
```python
for i in ['hamza', 'asif', 'junaid']: #block
    print(i)  #body
```

Output:
```
hamza
asif
junaid
```

*Example: string iterative data type*
```python
for i in "abcdef":
    print(i, "Hello") 
```

Output:
```
a Hello
b Hello
c Hello
d Hello
e Hello
f Hello
```