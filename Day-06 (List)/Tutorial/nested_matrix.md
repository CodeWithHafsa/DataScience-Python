# Nested matrix:
Matrix is a special case of two dimensional array where each data element is of strictly same size. So every matrix is also a two dimensional array.

*Example* :
```python
from numpy import *
a = array([['Mon',18,20,22,17],['Tue',11,18,21,18],
   ['Wed',15,21,20,19],['Thu',11,20,22,21],
   ['Fri',18,17,23,22],['Sat',12,22,20,18],
   ['Sun',13,15,19,16]])
m = reshape(a,(7,5))
print(m)
```

Output:
```
[
   ['Mon' '18' '20' '22' '17']
   ['Tue' '11' '18' '21' '18']
   ['Wed' '15' '21' '20' '19']
   ['Thu' '11' '20' '22' '21']
   ['Fri' '18' '17' '23' '22']
   ['Sat' '12' '22' '20' '18']
   ['Sun' '13' '15' '19' '16']
]
```

## Acessing Values:
The data elements in a matrix can be accessed by using the indexes.
*Example* :
```python
from numpy import * 
m = array([
   ['Mon',18,20,22,17],
   ['Tue',11,18,21,18],
   ['Wed',15,21,20,19],
   ['Thu',11,20,22,21],
   ['Fri',18,17,23,22],
   ['Sat',12,22,20,18],
   ['Sun',13,15,19,16]])
    
# Print data for Wednesday
print(m[2]) #access row two index element

# Print data for friday evening
print(m[4][3]) #acess row four and column three index element
```

Output:
```
['Wed', 15, 21, 20, 19]
23
```

## Adding a row:
To add a row in a matrix.

*Example* :
```python
from numpy import * 
m = array([['Mon',18,20,22,17],['Tue',11,18,21,18],
   ['Wed',15,21,20,19],['Thu',11,20,22,21],
   ['Fri',18,17,23,22],['Sat',12,22,20,18],
   ['Sun',13,15,19,16]])
m_r = append(m,[['Avg',12,15,13,11]],0)

print(m_r)
```

Output:
```
[
   ['Mon' '18' '20' '22' '17']
   ['Tue' '11' '18' '21' '18']
   ['Wed' '15' '21' '20' '19']
   ['Thu' '11' '20' '22' '21']
   ['Fri' '18' '17' '23' '22']
   ['Sat' '12' '22' '20' '18']
   ['Sun' '13' '15' '19' '16']
   ['Avg' '12' '15' '13' '11']
]
```
## Adding a column:
We can add column to a matrix using the insert() method.

*Example* :
```python
from numpy import * 
m = array([['Mon',18,20,22,17],['Tue',11,18,21,18],
   ['Wed',15,21,20,19],['Thu',11,20,22,21],
   ['Fri',18,17,23,22],['Sat',12,22,20,18],
   ['Sun',13,15,19,16]])
m_c = insert(m,[5],[[1],[2],[3],[4],[5],[6],[7]],1)

print(m_c)
```

Output:
```
[
   ['Mon' '18' '20' '22' '17' '1']
   ['Tue' '11' '18' '21' '18' '2']
   ['Wed' '15' '21' '20' '19' '3']
   ['Thu' '11' '20' '22' '21' '4']
   ['Fri' '18' '17' '23' '22' '5']
   ['Sat' '12' '22' '20' '18' '6']
   ['Sun' '13' '15' '19' '16' '7']
]
```

## Delete a row:
We can delete a row from a matrix using the delete() method.

*Example* :
```python
from numpy import * 
m = array([['Mon',18,20,22,17],['Tue',11,18,21,18],
   ['Wed',15,21,20,19],['Thu',11,20,22,21],
   ['Fri',18,17,23,22],['Sat',12,22,20,18],
   ['Sun',13,15,19,16]])
m = delete(m,[2],0)

print(m)
```

Output:
```
[
   ['Mon' '18' '20' '22' '17']
   ['Tue' '11' '18' '21' '18']
   ['Thu' '11' '20' '22' '21']
   ['Fri' '18' '17' '23' '22']
   ['Sat' '12' '22' '20' '18']
   ['Sun' '13' '15' '19' '16']
]
```

## Delete a column:
We can delete a column from a matrix using the delete() method. 

*Example* :
```python
from numpy import * 
m = array([['Mon',18,20,22,17],['Tue',11,18,21,18],
   ['Wed',15,21,20,19],['Thu',11,20,22,21],
   ['Fri',18,17,23,22],['Sat',12,22,20,18],
   ['Sun',13,15,19,16]])
m = delete(m,s_[2],1)

print(m)
```

Output:
```
[
   ['Mon' '18' '22' '17']
   ['Tue' '11' '21' '18']
   ['Wed' '15' '20' '19']
   ['Thu' '11' '22' '21']
   ['Fri' '18' '23' '22']
   ['Sat' '12' '20' '18']
   ['Sun' '13' '19' '16']
]
```

## Update a row:
To update the values in the row of a matrix we simply re-assign the values at the index of the row.

*Example* :
```python
from numpy import * 
m = array([['Mon',18,20,22,17],['Tue',11,18,21,18],
   ['Wed',15,21,20,19],['Thu',11,20,22,21],
   ['Fri',18,17,23,22],['Sat',12,22,20,18],
   ['Sun',13,15,19,16]])
m[3] = ['Thu',0,0,0,0]

print(m)
```

Output:
```
[
   ['Mon' '18' '20' '22' '17']
   ['Tue' '11' '18' '21' '18']
   ['Wed' '15' '21' '20' '19']
   ['Thu' '0' '0' '0' '0']
   ['Fri' '18' '17' '23' '22']
   ['Sat' '12' '22' '20' '18']
   ['Sun' '13' '15' '19' '16']
]
```