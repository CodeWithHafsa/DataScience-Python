# Regular Expression:
* A RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.
* RegEx can be used to check if a string contains the specified search pattern.
* Python has a built-in package called re, which can be used to work with Regular Expressions.

* We cannot pass 2 Flags in the same function but in different we can:
```
re.findall(pattern, string, re.Multiline)
re.findall(pattern, string, re.IGNORECASE)
```

---
Import the re module:
```python
import re
```
---
### Syntax:
```
re.findall(pattern, string, flag)
```
* pattern = the defined criteria of what we want to find or search. Pattern can be either Ordinary Characters or Special Characters. 
* string = the place from where we want to find.
* flag = Flag is if there is specific search criteria. Default is "False" which is 0. Flag = 1 is True.
---
