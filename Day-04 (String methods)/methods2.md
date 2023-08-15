### 23. format():
The format() method - Formats given values in a string

*Example*
```python
#named indexes:
txt1 = "My name is {fname}, I'm {age}".format(fname = "John", age = 36)
#numbered indexes:
txt2 = "My name is {0}, I'm {1}".format("John",36)
#empty placeholders:
txt3 = "My name is {}, I'm {}".format("John",36)
```

Output:
```markup
My name is John, I'm 36
My name is John, I'm 36
My name is John, I'm 36
```
___
### 24. format_map():
The format_map() method - Formats specified values in a string.

*Example*
```python
point = {'x':4,'y':-5}
print('{x} {y}'.format_map(point))

point = {'x':4,'y':-5, 'z': 0}
print('{x} {y} {z}'.format_map(point))
```

Output:
```
4 -5
4 -5 0
```