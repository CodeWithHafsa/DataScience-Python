# List and Array:
Lists are used to store multiple items in a single variable. Items in the list are enclosed between square brackets and separated by commas.

An array is a special variable, which can hold more than one value at a time.

|List                          |Array                        |
|-------------------------------|-----------------------------|
In-built data structure            | Need to import using array or numpy            |
Enclosed in square brackets            | Need to enclose using .array function             |
Can contain elements of different types (store homogenous values)            | Cannot contain elements of different types (store heterogenous values)             |
Cannot apply direct arithmetic operations            | Can apply direct arithmetic operations.             |
It consumes more memory (dynamic memory management)            | It consumes less memory comparatively             |
Can be printed without creating an explicit loop            | Need to create an explicit loop to print the array elements.             |
Length is not fixed (i.e. dynamic length)            | Length is fixed and should be decided before             |
List is slow as compared to array because it contains different types of data.            | Array is fast because everything is sorted in it.             |

*Example - List*

```python
#List
a = [1, "Yash", ['a', 'e']] 
print(type(a))
print(a)
```

Output:
```
<class 'list'>
[1, 'Yash', ['a', 'e']]
```

*Example - Array*
```python
# importing "array" for array creations
import array as arr
  
# creating an array with integer type
a = arr.array('i', [1, 2, 3])
print(type(a))
for i in a:
    print(i, end=" ")
```

Output:
```
<class 'array.array'>
1 2 3 
```

## Key Points:
* Post-processing - data processing after output
* Pre-processing - data before processing
* Operations/Function can be: in-line operations or in-memory operations. 