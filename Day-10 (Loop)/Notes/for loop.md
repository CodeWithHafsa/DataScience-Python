# For loop:
A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

Syntax:
```
for (counter;logic;inc/dec)
    {body}
```

*Example 01* :
```python
names = ['a','b','c','d','e','f','g']

for name in names:
    print(name)
```

Output:
```
a
b
c
d
e
f
g
```
=========================================================
*Example 02* :
```python
names = ['a','b','c']

for name in names:
    print(f'Hello Mr/Miss, {name}, Welcome in our AI Class!')
```

Output:
```
Hello Mr/Miss, a, Welcome in our AI Class!
Hello Mr/Miss, b, Welcome in our AI Class!
Hello Mr/Miss, c, Welcome in our AI Class!
```

=========================================================
*Example 03* :\
Print names, ages and courses in zip file using for loop.

```python
names = ['ali','hamza','junaid']
ages = [22,25,30]
courses = ['AI',"ML","DS"]

for name,age, course in zip(names,ages,courses):
    print(f'Hello Dear {name}, Welcome in {course} Course class, your are {age} years old')
```

Output:
```
Hello Dear ali, Welcome in AI Course class, your are 22 years old
Hello Dear hamza, Welcome in ML Course class, your are 25 years old
Hello Dear junaid, Welcome in DS Course class, your are 30 years old
```

## The break statement:
With the break statement we can stop the loop before it has looped through all the items:

* When print statement is written after `for` loop, then break statement - breaks the list after 'banana', means it returns 'apple and banana'.
```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x) 
  if x == "banana":  
    break
```

Output:
```
apple
banana
```

* When print statement is written after `break` statement, then break statement - breaks the list before 'banana', means it only return 'apple'.

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break
  print(x) 
```

Output:
```
apple
```

## The continue Statement
With the continue statement we can stop the current iteration of the loop, and continue with the next:

*Example* :\
In the below example, the continue statement skips 'banana' from the lists and only prints 'apple and cherry'.

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x) 
```

Output:
```
apple
cherry
```
## The range function:
The range() function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and ends at a specified number.
*Example 01* :
```python
for x in range(3):
  print(x) 
```

Output:
```
1
2
3
```

=========================================================
*Example 02* :
```python
for x in range(2, 6):
  print(x) 
```

Output:
```
2
3
4
5
```

=========================================================
*Example 03* :
```python
for x in range(2, 15, 3): #print numbers from 2 to 30 with the difference of 3
  print(x) 
```

Output:
```
2
5
8
11
14
```

## Else in For Loop
The else keyword in a for loop specifies a block of code to be executed when the loop is finished:

*Examples* :
* Print all numbers from 0 to 5, and print a message when the loop has ended:
```python
for x in range(3):
  print(x)
else:
  print("Finally finished!")
```

Output:
```
0
1
2
3
Finally finished!
```

* Break the loop when x is 3, and see what happens with the else block:
```python
for x in range(6):
  if x == 3: break
  print(x)
else:
  print("Finally finished!")
```

Output:
```
0
1
2
```

## Nested for Loop:
A nested loop is a loop inside a loop.
The "inner loop" will be executed one time for each iteration of the "outer loop":

*Example* :
```python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)
```

Output:
```
red apple
red banana
red cherry
big apple
big banana
big cherry
tasty apple
tasty banana
tasty cherry
```

## The pass Statement
`for` loops cannot be empty, but if you `for` some reason have a `for` loop with no content, put in the pass statement to avoid getting an error.

*Example* :
```python
for x in [0, 1, 2]:
  pass
# having an empty for loop like this, would raise an error without the pass statement
```

Output:
```

```