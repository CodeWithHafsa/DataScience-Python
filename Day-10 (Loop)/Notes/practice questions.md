## Practice Questions:
*Example 01* :\
Create a user interface for username and password using for loop.
```python
users = ['a','b','c']
password = ['1','2','3']

ui = input("UserName:\t")
pi = input("Password:\t")

for u,p in zip(users,password):
    if ui == u and pi == p:
        print(f"Welcome Dear {u}!")
        break
        
else:
    print("Not Valid user name password!")
```

Output:
* If input: ui=a and pi = 1
```
Welcome Dear a!
```

* If input ui= admin and pi = admin123
```
Not Valid user name password!
```
=========================================================
*Example 02* :\
Create a user interface in which system only welcomes valid customers and block customers could not enter in the system.
```python
names = list('abcdefghij')
blocked_customer = ['b','g','h']

for name in names:
    if name not in blocked_customer:
        print(f'Hello {name}!')
```

Output:
```
Hello a!
Hello c!
Hello d!
Hello e!
Hello f!
Hello i!
Hello j!
```
---
### Create Data Enter System using loop
Information: you can enter records unit your "enter" exit|x.

```python
data = []

while True:
    n = input("name")
    p = input("password")
    if n=='exit' or n == 'x':
        break
        
    data.append([n,p])
```

Output:
```
[['admin1', 'password1'], ['admin2', 'password2'], ['admin3', 'password3']]
```

----
### Zip method in list:
The zip() function returns a zip object, which is an iterator of tuples where the first item in each passed iterator is paired together, and then the second item in each passed iterator are paired together etc.

*Example 01* :
```python
a = [1,2,3]
b = ['a','b','c']
list(zip(a,b))
```

Output:
```
[(1, 'a'), (2, 'b'), (3, 'c')]
```
=========================================================
*Example 02* :

```python
names = ['ali','hamza','junaid']
ages = [22,25,30]
courses = ['AI',"ML","DS"]

data = list(zip(names,ages,courses))
print(data)
```

Output:
```
[('ali', 22, 'AI'), ('hamza', 25, 'ML'), ('junaid', 30, 'DS')]
```

* TO unzip the list or dictionary:
```python
a,b,c = [1,2,3] # unzip

print(a)
print(b)
print(c)
```

Output:
```
1
2
3
```
----
### Enumerate method in list:
Enumerate() method adds a counter to an iterable and returns it in a form of enumerating object. This enumerated object can then be used directly for loops or converted into a list of tuples using the list() function.

*Example* :
```python
#         0      1.      2
names = ['ali','hamza','junaid']
list(enumerate(names))
```

Output:
```
[(0, 'ali'), (1, 'hamza'), (2, 'junaid')]
```
----
### Idx method in list:
The Python index() method helps you find the index position of an element or an item in a string of characters or a list of items. 
```python
names = ['ali','hamza','junaid']
for idx, value in enumerate(names):
    print(idx, value)
```

Output:
```
0 ali
1 hamza
2 junaid
```