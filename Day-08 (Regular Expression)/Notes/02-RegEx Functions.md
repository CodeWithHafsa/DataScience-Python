# RegEx Functions:
The re module offers a set of functions that allows us to search a string for a match:

|   Function             |Description                           |             
|----------------|-------------------------------|
|`findall`| Returns a list containing all matches           |
|`search`| Returns a Match object if there is a match anywhere in the string           |
|`split`| Returns a list where the string has been split at each match           |
|`sub`| Replaces one or many matches with a string          |


## 1. The findall() Function:
The findall() function returns a list containing all matches.

*Example 01* :
```python
import re

#Return a list containing every occurrence of "ai":
txt = "The rain in Spain"
x = re.findall("ai", txt)
print(x)
```

Ouput:
```
['ai', 'ai']
```
=========================================================
* If no matches are found, an empty list is returned.

*Example 02* :
```python
import re

txt = "The rain in Spain" # If no matches are found

#Check if "Portugal" is in the string:
x = re.findall("Portugal", txt)
print(x)

if (x):
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output:
```
[]
No match
```

## 2. The search() Function:
The search() function searches the string for a match, and returns a Match object if there is a match.
* If there is more than one match, only the first occurrence of the match will be returned.

*Example 01* :
```python
import re

txt = "The rain in Spain" #for more than one match
x = re.search("\s", txt)

print("The first white-space character is located in position:", x.start())
```

Output:
```
The first white-space character is located in position: 3
```
=========================================================
* If no matches are found, the value None is returned.

*Example 02* :
```python
import re

txt = "The rain in Spain" # If no matches are found
x = re.search("Portugal", txt)
print(x)
```

Output:
```
None
```

## 3. The split() Function:
The split() function returns a list where the string has been split at each match:

*Example 01* :
```python
import re

#Split the string at every white-space character:
txt = "The rain in Spain"
x = re.split("\s", txt)
print(x)
```

Output:
```
['The', 'rain', 'in', 'Spain']
```

=========================================================
* You can control the number of occurrences by specifying the `maxsplit` parameter:

*Example 02* :
```python
import re

#Split the string at the first white-space character:
txt = "The rain in Spain"
x = re.split("\s", txt, 1) #here maxsplit=1
print(x)
```

Output:
```
['The', 'rain in Spain']
```

## 4. The sub() Function:
The sub() function replaces the matches with the text of your choice:

*Example 01* :
```python
import re

#Replace all white-space characters with the digit "9":
txt = "The rain in Spain"
x = re.sub("\s", "9", txt)
print(x)
```

Output:
```
The9rain9in9Spain
```
=========================================================
* You can control the number of replacements by specifying the count parameter:

*Example 02* :
```python
import re

#Replace the first two occurrences of a white-space character with the digit 9:
txt = "The rain in Spain"
x = re.sub("\s", "9", txt, 2) #here count=2
print(x)
```

Output:
```
The9rain9in Spain
```