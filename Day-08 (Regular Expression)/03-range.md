# Range group of charachers:

* *Example 01*:
```python
text = """Python Langauge123
"""

# pattern = r"[0123456789]+" #print line that include letters from 1to9
# pattern = r"[0-9]+"        #print line that include letters from 1to9
# pattern = r"[A-za-z]+"     #print line that include letters from A-Z or a-z
# pattern = r"[A-z]+"        #print line that include letters from A-Z or a-z
#pattern = r"[A-z0-9]+"       #print line that include letters from A-Z or a-z or 0-9
pattern = r"[A-z0-1]+"       #print line that include letters from A-Z or a-z or 0-1

l = re.findall(pattern, text)
print(l)
```

Output:
```
['Python', 'Langauge1']
```

=========================================================

* *Example 02*:
```python
text = """We love our country Pakistan Zinda bad!
pakistan one of. & the best contry in the world!
Hello Wolrd 7.2 
222.27
222,772
I'm living in pakistan
Rs. 277
 aljdkjfajdfj asdlkj 702
"""

pattern = r"[0-9.,]+" #print line that includes number from 0to9 or dot or comma
l = re.findall(pattern, text)
print(l)
```

Output:
```
['.', '7.2', '222.27', '222,772', '.', '277', '702']
```

# ? optional:
If we use question mark (?) in pattren, it means that we don't have to write pattren. It includes all kinds of pattrens. 

```
[0-9] = \d
[A-z] = \w
```

*Example 01* :
```python
text = """
purchase data 01*12*2023
purchase data 01/12/2023
purchase data 01/12/2023
puchase date 24-12-2023
puchase date 28-12-2023
"""

#pattern = r"\d{1,2}[*-/]\d{1,2}[*-/]\d{2,4}" #print different types of pattrens
pattern = r"\d{1,2}[*-?]\d{1,2}[*-?]\d{2,4}" #print different types of pattrens using question mark
l = re.findall(pattern, text)
print(l)
```

Output:
```
['01*12*2023', '01/12/2023', '01/12/2023', '24-12-2023', '28-12-2023']
```

# Word boundary concept:
* \b \b
* If you want to apply boundayr concept you have to use "r" befor pattern

*Example 01* :
```python
text = """
pakistan zinda bad
pakab adkajdskfj asdjl
paik hellow
pakanandan kajsdf alsdjfa
pak aksdjfkasd fas
"""

pattern = r"\bp.+n\b" #print letters that starts with 'p' and ends at 'n'
l = re.findall(pattern, text, re.M) 
print(l)
```

Output:
```
['pakistan', 'pakanandan']
```
=========================================================

* *Example 02*:
```python
text = """
pakistan zinda bad
pakab adkajdskfj asdjl
pik hellow
"""

pattern = "p.+k" #print letters that starts with 'p' and ends at 'k'
l = re.findall(pattern, text, re.M) 
print(l)
```

Output:
```
['pak', 'pakab adkajdsk', 'pik']
```