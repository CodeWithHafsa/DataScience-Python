# List Data Type:
* Heterogenous data type
* Dynamic length
* Dynamic memory management

Syntax:
```[element1, element2, element3,..... ]``` - Square bracket

1. One to One Realtion: Means only one variable relates to one value.
2. One to Many Relation: Means only one variable relates to many value.

*Example: One to One Relation*
```python
s_1name = "Hammad" 
s_2name = "Visha"
s_3name = "Sadia"
s_4name = "M.A Rasheed"
print(s_1name)
print(s_2name)
print(s_3name)
print(s_4name)
```

Output:
```
Hammad
Visha
Sadia
M.A Rasheed
```

*Example: One to Many Relation*
```python
#           0          1        2          3  (positive indexing)
names = ["Hammad", "Vishal", "Sadia", "M.A Rasheed"]
#          -4         -3        -2         -1  (negative indexing)
print(names)
```

Output:
```
['Hammad', 'Vishal', 'Sadia', 'M.A Rasheed']
```

* Negative indexing - starts with -1
* Positive indexing - starts with 0

# Extract value from iterative data type with index position:

Syntax : ```list_variable[index_number]```

*Example*
```python
names1 = input("Please insert names with ',' seprated: ")
print(names1)
names1.split(",") #split is 'in-line function'
```

Output:
```
Hamza,Ali,Iqbal,Junaid,Ibad,Konain

['Hamza', 'Ali', 'Iqbal', 'Junaid', 'Ibad', 'Konain']
```

*Example : Indexing*
```python
#           0          1        2          3  (positive indexing)
names = ["Hammad", "Visha", "Sadia", "M.A Rasheed"]
#          -4         -3        -2         -1  (negative indexing)

# list_variable[index_number]
print(names[1])
print(names[-3])
```

Output:
```
Visha
Visha
```

# Slicing
A slice object is used to specify how to slice a sequence. Slicing can be: Positive or Negative.

It is used to return a particular range value.

Syntax: ```list_variable[start:end:step]```
* start = this number will be included
* end = this number will be excluded - i.e. end-1
* step = sequence/gap
  * step = 1 (positive value - means left to right) #it is by-default
  * step = -1 (negative value - means right to left) 
