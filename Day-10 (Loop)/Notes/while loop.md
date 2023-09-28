# Loop:
Looping means repeating something over and over until a particular condition is satisfied.\
There are two types of loops:
1. while loop
2. for loop

* Some controls of loop:
     - break statement
     - continue statement
     - pass statement

# While loop:
With the while loop we can execute a set of statements as long as a condition is true.

* There are three important things in while loop:
     - counter
     - logic
     - increment / decrement (if we don't write increment or decrement, it will create infinite loop. That is difficult to handle.)

*Example 01* :\
It prints counting from 1 to 10 and after that prints "Hello".

```python
counter = 0 # counter

while counter <= 10: # logic
    print(counter)
    counter += 1  #increment
else:
    print("Hello")
```

Output:
```
0
1
2
3
4
5
6
7
8
9
10
Hello
```
=========================================================
*Example 02* :\
Due to decrement, it prints reverse counting i.e. from 10 to 1.
```python
counter = 10      #counter
while counter > 0:  #logic
    print(counter)
    counter -= 1   #decrement
```

Output:
```
10
9
8
7
6
5
4
3
2
1
```

## The break statement:
With the break statement we can stop the loop even if the while condition is true:

*Example 01* :\
In the below example, according to logic loop prints counting from 1 to 100, but due to break statement counter == 5, it only prints counting from 1 to 5.
```python
counter = 1       #counter
while counter < 100:   #logic
    print(counter)
    if counter == 5:
        break       #break statement
    counter += 1    #increment
```

Output:
```
1
2
3
4
5
```
=========================================================
*Example 02* :\
In the below example, according to logic loop prints counting from 1 to 6, but due to break statement counter == 3, it only prints counting from 1 to 3.
```python
i = 1
while i < 6:
  print(i)
  if (i == 3):
    break
  i += 1
```

Output:
```
1
2
3
```

## The continue statement:
With the continue statement we can stop the current iteration, and continue with the next:

*Example 01* :\
In the below example, according to logic loop prints counting from 1 to 10, but due to continue statement counter == 3, it skips 3 from the  counting.

```python 
i = 0      #counter
while i < 9:   #logic
    i += 1    #increment
    if i == 3:
        continue # ignore everything in block below for this step only
    print(i)
```

Output:
```
1
2
4
5
6
7
8
9
```
=========================================================
*Example 02* :\
In the below example, according to logic loop prints counting from 1 to 6, but due to continue statement counter == 3, it skips 3 from the  counting.

```python
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```

Output:
```
1
2
4
5
6
```

## The else statement:
We can use `else` with while statement. With the else statement we can run a block of code once when the condition no longer is true:

*Example* :
```python
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
```

Output:
```
1
2
3
4
5
i is no longer less than 6
```

## Practice Questions:
=========================================================
*Example* :\
Print alphabets from a to g using `while` loop using increment:
```python
#index  1   2   3   4   5   6   7
#len.   0.  1.  2.  3   4   5   6
name = ['a','b','c','d','e','f','g']

#print(len(name)) #output 6

i = 0
while i < len(name): # dyamic length
    print(name[i])
    i += 1
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
*Example* :\
Print alphabets from a to g using `while` loop using decrement:

```python
#count   1.  2.  3.  4   5   6   7
#index   0.  1.  2.  3.  4.  5.  6.
name = ['a','b','c','d','e','f','g']

#print(len(name)) #output 7

i = len(name)-1

while i >= 0: # dyamic length
    print(name[i])
    i -= 1
```

Output:
```
g
f
e
d
c
b
a
```
=========================================================
*Example* :\
Print year from 1980 to 2023 using `while` loop:

```python
year = 2023

while year >= 1998:
    print(year)
    year -= 1
```

Output:
```
2023
2022
2021
2020
2019
2018
2017
2016
2015
2014
2013
2012
2011
2010
2009
2008
2007
2006
2005
2004
2003
2002
2001
2000
1999
1998
```