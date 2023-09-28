# Python Lambda:
A lambda function is a small anonymous function.\
A lambda function can take any number of arguments, but can only have one expression.

It is a:
* one line function
* without name
* did'nt use before or it'll not be used in future

Syntax:
* Syntax of normal function
```
def add_two_numbers(x,y):
    return x + y
```
* Syntax of lambda function
```
lambda x,y : x + y
```
*Example 01* :
* *Example - Using normal function* :
```python
def add_two_numbers(x,y):
    return x + y

add_two_numbers(7,2)
```

Output:
```
9
```
* *Example - Using lambda function* :
```python
a = lambda x,y : x + y
print(a(2,7))
```

Output:
```
9
```
=========================================================
*Example 02* :
```python
data = [[1,'Z',"E"],
       [3,'X',"F"],
       [2,"Y","G"]]

print(sorted(data, key=lambda k:k[0]))  #sort matrix according to index=0 (in column)

#print(sorted(data, key=lambda x:x[1]))  #sort matrix according to index=1 (in column)
#output: [[3, 'X', 'F'], [2, 'Y', 'G'], [1, 'Z', 'E']]
```

Output:
```
[[1, 'Z', 'E'], [2, 'Y', 'G'], [3, 'X', 'F']]
```

# Some Practice Questions:
* Add 10 to argument a, and return the result:
```python
 x = lambda a: a + 10
print(x(5))
```

Output:
```
15
```

---
* Multiply argument a with argument b and return the result:
```python
x = lambda a, b: a * b
print(x(5, 6))
```

Output:
```
30
```

---
* Summarize argument a, b, and c and return the result:
```python
x = lambda a, b, c: a + b + c  # sum
print(x(5, 6, 2))
```

Output:
```
13
```

---
* Use that function definition to make a function that always doubles / triples the number you send in:
```python
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)    #to double the number   #output=22
# mytripler = myfunc(3)  #to triple the number   #output=33
print(mydoubler(11))
```

Output:
```
22
```