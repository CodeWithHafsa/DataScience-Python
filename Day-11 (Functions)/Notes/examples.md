# Examples:

## Required Parameter/Arguments:
Required arguments, as the name suggests, are those that are required to be passed to the function at the time of function call. 

*Example 01* :
```python
def add_two_numbers(num1,num2):   #function signature
    return num1 + num2

print(add_two_numbers(8,2))
print(add_two_numbers(20,7))
```

Output:
```
10
27
```
=========================================================
*Example 02* :
```python
def add_two_numbers(num1,num2):#function signature
    print(f'numbe1: {num1} and number2: {num2}')
    return num1 + num2

print(add_two_numbers(7,8))
print(add_two_numbers(20,7))
```

Output:
```
numbe1: 7 and number2: 8
15
numbe1: 20 and number2: 7
27
```

## Keyword Parameter/Arguments:
With keyword arguments in python, we can change the order of passing the arguments without any consequences.

*Example 01* :
```python
def add_two_numbers(num1,num2):#function signature
    print(f'numbe1: {num1} and number2: {num2}')
    return num1 + num2

print(add_two_numbers(num2=7, num1=8))
print(add_two_numbers(num1=20, num2=7))
```

Output:
```
numbe1: 8 and number2: 7
15
numbe1: 20 and number2: 7
27
```
=========================================================
*Example 02* :
```python
def abc(x,y,z=0):
    return x+y+z

print(abc(1,2))
print(abc(1,2,3))
```

Output:
```
3
6
```
=========================================================
*Example 03* :
```python
def abc(x,y=0,z=0):
    return x+y+z

print(abc(1,2))
print(abc(1,2,3)) # postional arguments
print(abc(z=2,x=2,y=3)) # key word arguments
print(abc(2))
# print(abc())   #throws an error b/c x is not defined
```

Output:
```
3
6
7
2
```

## Arbitary Parameter/Arguments:
*Example 01* :

```python
l = ("a",'b','c')
 
print(l[0],l[1],l[2])    #basic python
print(*l) #using arbitary argument
```

Output:
```
a b c
a b c
```
=========================================================
*Example 02* :
```python
def abc(x,y=0,z=0):  #function defining
    return x + y + z   #return statement

d = {"x":7,   #dictionary
    "y":20,
    "z":30 }

print(d['x'], d['y'], d['z'])    #using normal python, it print list

print(abc(d['x'], d['y'], d['z']))    # using normal python, it add value given in function as defined in return statement

print(abc(x=7, y=20, z=30))   #using keyword argument, it add the value given in print function as defined in return 

print(abc(**d))  #using arbitary argument, it add value given in function as defined in return statement
```

Output:
```
7 20 30
57
57
57
```
---
# Some Extra Unlimited argument function Examples:

*Example 01* :
```python
def my_sum(*nums):
    
    total = 0
    
    for n in nums:
        total += n
    return total

print(my_sum(1,2,2,6,2,20)) #sum of all numbers = 33
```

Output:
```
33
```
=========================================================
*Example 02* :
```python
l1 = [1,23,23]
print(my_sum(*l1))  #using my_sum function defined in example-01, sum of all numbers = 47
```

Output:
```
47
```
=========================================================
*Example 03* :
```python
print(1,2,2,3,4)
print(1,2,2,3,4, sep='**')  #separated numbers using **
```

Output:
```
1 2 2 3 4
1**2**2**3**4
```
=========================================================
*Example 04* :
```python
data = input("Enter Name,Father,Course").split(",")
print(data)   #split name using comma
```

Output:
```
Enter Name,Father,CourseQasim,Aslam,AI

['Qasim', 'Aslam', 'AI']
```

## Example of arbitary argument and keyvalues:
*Example 01* :
```python
def abc(**data):
    print(data)
    return list(data.items())

#   key=value
abc(x=20,y=3, e=200, end=200)
```

Output:
```
{'x': 20, 'y': 3, 'e': 200, 'end': 200}

[('x', 20), ('y', 3), ('e', 200), ('end', 200)]
```
=========================================================
*Example 02* :
```python
data = input("Enter Name,Father,Course").split(",")
data1 = {"Name":data[0],
       "Father":data[1],
       "Course":data[2]}

abc(**data1)
```

Output:
```
Enter Name,Father,CourseQasim,Aslam,AI
{'Name': 'Qasim', 'Father': 'Aslam', 'Course': 'AI'}

[('Name', 'Qasim'), ('Father', 'Aslam'), ('Course', 'AI')]
```

## Some Advance Examples:
* positional unlimited arguments
* key=word umlimited arguments

*Example 01* :

```python
def advance(x, y, *nums, **data):  # In one function the arbitary args(*) and kwargs (**) arguments can use only one time, it cannot repeat. 
    print(x,y)
    print(nums)
    print(data)
    
advance(2,7, 'a',2,2,20,'b', e=20, c=2)
# here x=2 and y=7 (positional arguments)
# here *nums = 'a',2,2,20,'b'
# here **data = e=20, c=2 (dictionary - due to equal to sign it print keyvalues i.e. keyword argument)
```

Output:
```
2 7
('a', 2, 2, 20, 'b')
{'e': 20, 'c': 2}
```

=========================================================
*Example 02* :
```python
def advance(x, y, *nums, **data):  # In one function the arbitary args(*) and kwargs (**) arguments can use only one time, it cannot repeat. 
    print(x,y)
    print(nums)
    print(data)

l1 = [2,2,3]
l2 = [4,4,4]

print(advance(7,2,*l1,*l2))
# here x=7 and y=2
# here *l1 and *l2 - merged both l1 and l2 list
# here *nums = { }
# here **data = None
```

Output:
```
7 2
(2, 2, 3, 4, 4, 4)
{}
None
```