# Ascii Code:
ASCII stands for American Standard Code for Information Interchange. It is a numeric value given to different characters and symbols, for computers to store and manipulate.
* A = 65
* Z = 90
* a = 97
* z = 122
* 0 = 47
* 9 = 58

*Example* :
```python
# Program to find the ASCII value of the given character

c = 'p'
print("The ASCII value of '" + c + "' is", ord(c))
```

Output:
```
The ASCII value of 'p' is 112
```

### *Example: To generate alphabets using ascii code list*:

* Method-01:
```python
l = list(range(65,91))
for a in l:
    print(chr(a))
```

Output:
```
A
B
C
D
E
F
G
H
I
J
K
L
M
N
O
P
Q
R
S
T
U
V
W
X
Y
Z
```

* Method-02:
```python
[chr(i) for i in range(65,91)] #alphabetic list
```

Output:
```
['A',
 'B',
 'C',
 'D',
 'E',
 'F',
 'G',
 'H',
 'I',
 'J',
 'K',
 'L',
 'M',
 'N',
 'O',
 'P',
 'Q',
 'R',
 'S',
 'T',
 'U',
 'V',
 'W',
 'X',
 'Y',
 'Z']
```
---
### *Example: To access a alphabet using ascii code*:

```python
chr(67)
```

Output:
```
'C'
```
---
### *Example: To know asciss code of a alphabet *:

```python
ord('Z')
```

Output:
```
90
```
========================================================

## Data Frame Example:
```python
import pandas as pd

data = {"roll_no":[1,2,3],
       "name":['a','b','c'],
       'course':['AI',"DS","ML"]}

print(data)

df = pd.DataFrame(data)
df
```

Output:
```
{'roll_no': [1, 2, 3], 'name': ['a', 'b', 'c'], 'course': ['AI', 'DS', 'ML']}
```
<img src="pandas.png" class="img-responsive" alt=""> </div>

## CNIC Comparision:

1. Bank data is not equal to customer data - False
2. Add '-' in customer data, so bank data become equal to customer data - True
3. Remove '-' in bank data, so bank data become equal to customer data - True
4. Use of replace function, so bank data become equal to customer data - True

```python
#       Bank                  customer
print('42201-7578760-1' == '4220175787601') #real data

print('42201-7578760-1' == '42201-7578760-1') # after converted 1
print('4220175787601' == '4220175787601') # after coverted 2

print('42201-7578760-1'.replace("-","") == '4220175787601'.replace("-","")) #3
```

Output:
```
False
True
True
True
```