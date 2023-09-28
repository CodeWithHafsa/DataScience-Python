# Generator Function:
In Python, a generator is a function that returns an iterator that produces a sequence of values when iterated over.

```python
def my_range(start,end,step=1):
    for i in range(start,end+1, step):
        yield i
            
a = my_range(1,11)
print(next(a))
print(next(a)) #until print function not written again, it doesnot execute next step
print(next(a)) 
```

Output:
```
1
2
3
```

* After print some other function, we can continue the work and print previous function.
```python
print("Hello!")
print(next(a))
```

Output:
```
Hello!
4
```

## Create Python Generator:
In Python, similar to defining a normal function, we can define a `generator` function using the def keyword, but instead of the `return` statement we use the `yield` statement.

```python
def generator_name(arg):
    # statements
    yield something
```
Here, the `yield` keyword is used to produce a value from the generator.

When the generator function is called, it does not execute the function body immediately. Instead, it returns a generator object that can be iterated over to produce the values.

*Example* :
```python
def my_generator(n):

    # initialize counter
    value = 0

    # loop until counter is less than n
    while value < n:

        # produce the current value of the counter
        yield value

        # increment the counter
        value += 1

# iterate over the generator object produced by my_generator
for value in my_generator(3):

    # print each value produced by generator
    print(value)
```

Output:
```
0
1
2
```

## Shorthand - Generator Expression Syntax:
A generator expression has the following syntax,

```python
(expression for item in iterable)
```
Here, `expression` is a value that will be returned for each item in the iterable.

*Example* :
```python
# create the generator object
squares_generator = (i * i for i in range(5))

# iterate over the generator and print the values
for i in squares_generator:
    print(i)
```

Output:
```
0
1
4
9
16
```

# Recursion Function:
Python also accepts function recursion, which means a defined function can call itself.

*Example 01* :
```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

# Test the function
number = 5
result = factorial(number)
print(f"The factorial of {number} is {result}")
```

Output:
```
The factorial of 5 is 120
```
========================================================= 
*Example 02* :
```python
def tri_recursion(k):
  if(k > 0):
    result = k + tri_recursion(k - 1)
    print(result)
  else:
    result = 0
  return result

print("\n\nRecursion Example Results")
tri_recursion(6)
```

Output:
```


Recursion Example Results
1
3
6
10
15
21
```