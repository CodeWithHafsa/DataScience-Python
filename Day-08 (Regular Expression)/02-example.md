## We have some special character for special purpose:
```
. any thing except \n
* zero or many
+ one or many
^ start line with
$ ending ling
*+ pick the pattren which written before +
```

Syntax:
```
pattren = [pattren, text, flag]
flag = 0 means (no flag)
```

# Examples:
*Example 01*:
```python
text = """We love our country! Pakistan Zinda bad! 
pakistan one of the best contry in the world!"""
pattern = "Pakistan" # character sequances
#pattern = "Pa" # character sequances
#pattern = "a" # character sequances
re.findall(pattern,text)
```

Output:
```
['Pakistan']
```
=========================================================

*Example 02*:
```python
text = """We love our country! Pakistan Zinda bad! 
pakistan one of the best contry in the world!"""
pattern = "r" # character sequances
re.findall(pattern,text)
```

Output:
```
['r', 'r', 'r', 'r']
```
=========================================================

*Example 03*:

re.Ignorance - means it ignores upper and lower alphabet order and prints all words that are according to pattren in the given text.

```python
text = """We love our country! Pakistan Zinda bad! 
pakistan one of the best contry in the world!"""
# display(text)
pattern = "Pakistan" # character sequances
re.findall(pattern, text, re.IGNORECASE)
```

Output:
```
['Pakistan', 'pakistan']
```
=========================================================

### - *Use of 'dot'* :
*Example 04*:
```python
text = """Python Language"""
display(text)
pattern = "." #dot means it takes all character individually
re.findall(pattern, text, re.IGNORECASE)
```

Output:
```
'Python Language'
['P', 'y', 't', 'h', 'o', 'n', ' ', 'L', 'a', 'n', 'g', 'u', 'a', 'g', 'e']
```
=========================================================

*Example 05*:
```python
text = """Python Language"""
# display(text)
pattern = "....." #five dots means it return 5words in one line including space 
re.findall(pattern, text, re.IGNORECASE)
```

Output:
```
['Pytho', 'n Lan', 'guage']
```

=========================================================
### - *Use of 'dot and plus sign'* :
*Example 06*:
```python
text = """We love our country! Pakistan Zinda bad! 
pakistan one of the best contry in the world!
Hello Wolrd"""
# display(text)

# + mean pick the pattern which written before "+"
pattern = ".+" # character sequances
re.findall(pattern, text, re.IGNORECASE)
```

Ouput:
```
['We love our country! Pakistan Zinda bad! ',
 'pakistan one of the best contry in the world!',
 'Hello Wolrd']
```
=========================================================

*Example 07*:
```python
text = """We love our country! Pakistan Zinda bad! 
pakistan one of the best contry in the world!
Hello Wolrd"""
# display(text)

# + mean pick the pattern which written before "+"
pattern = "c.+" #prints pattren starting with c and ends at new line
re.findall(pattern, text, re.IGNORECASE)
```

Output:
```
['country! Pakistan Zinda bad! ', 'contry in the world!']
```

=========================================================
### - *Made a pttren in which print lines that are ending at new line* :
*Example 08*:\
re.Multiline - means use if we use write many lines in the given text.

```python
text = """We love our country Pakistan Zinda bad!
pakistan one of the best contry in the world!
Hello Wolrd
I'm living in pakistan

Lorem ipsum dolor sit amet, consectetur adipiscing elit.!
Nullam quis ligula sit amet leo rutrum consectetur ac vitae sapien
Suspendisse ac tellus dictum, bibendum massa eget, dapibus mauris.
Sed in dui vel odio pharetra elementum sit amet vitae lorem.
Praesent pellentesque mi nec lorem sollicitudin gravida.!
"""
# display(text)

# + mean pick the pattern which written before "+"
#pattern = ".+n$" # character sequances
pattern = ".+!$" # character sequances

re.findall(pattern, text, re.MULTILINE) #multiline use if we use write many lines
```

Output:
```
['We love our country Pakistan Zinda bad!',
 'pakistan one of the best contry in the world!',
 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.!',
 'Praesent pellentesque mi nec lorem sollicitudin gravida.!']
```
----

### - Convert any special meaning character into normal character place " \ "  before special charachter
* *Example 01: Print lines that ends at full stop*:
```python
text = """
Lorem ipsum dolor sit amet, consectetur adipiscing elit.!
Nullam quis ligula sit amet leo rutrum consectetur ac vitae sapien
Suspendisse ac tellus dictum, bibendum massa eget, dapibus mauris.
Sed in dui vel odio pharetra elementum sit amet vitae lorem.
Praesent pellentesque mi nec lorem sollicitudin gravida.!
"""
# display(text)

pattern = ".+\.$" #print lines that ends at full stop

re.findall(pattern, text, re.MULTILINE)
```

Output:
```
['Suspendisse ac tellus dictum, bibendum massa eget, dapibus mauris.',
 'Sed in dui vel odio pharetra elementum sit amet vitae lorem.']
```
=========================================================

* *Example 02: Print lines that ends at excalmation mark*:
```python
text = """we love our country! Pakistan zinda bad!
pakistan one of the best contry in the world!
Hello world
i am living in pakistan!"""

# display (text) 
pattern = ".*!$"  # print lines that ends at excalmation mark
re.findall(pattern,text,re.M)
```

Output:
```
['we love our country! Pakistan zinda bad!',
 'pakistan one of the best contry in the world!',
 'i am living in pakistan!']
```

=========================================================

* *Example 03: Print lines that starts with 'P' ends at excalmation mark*:

```python
text = """We love our country Pakistan Zinda bad!
pakistan one of the best contry in the world!
Hello Wolrd
I'm living in pakistan

Lorem ipsum dolor sit amet, consectetur adipiscing elit.!
Nullam quis ligula sit amet leo rutrum consectetur ac vitae sapien
Suspendisse ac tellus dictum, bibendum massa eget, dapibus mauris.
Sed in dui vel odio pharetra elementum sit amet vitae lorem.
Praesent pellentesque mi nec lorem sollicitudin gravida.!
"""
# display(text)

pattern = "^P.+!$" #print lines that starts with 'P' ends at excalmation mark
re.findall(pattern, text, re.MULTILINE)
```

Ouput:
```
['Praesent pellentesque mi nec lorem sollicitudin gravida.!']
```
=========================================================

* *Example 04: Print lines that starts with 'P or p' ends at excalmation mark*:

```python
text = """We love our country Pakistan Zinda bad!
pakistan one of the best contry in the world!
Hello Wolrd
I'm living in pakistan

Lorem ipsum dolor sit amet, consectetur adipiscing elit.!
Nullam quis ligula sit amet leo rutrum consectetur ac vitae sapien
Suspendisse ac tellus dictum, bibendum massa eget, dapibus mauris.
Sed in dui vel odio pharetra elementum sit amet vitae lorem.
Praesent pellentesque mi nec lorem sollicitudin gravida.!
"""

text = text.lower()
# lower -use to convert all text to lower letters, so all lines that starts with p whether it is capital P or small p could print.
# display(text)

pattern = "^p.+!$" # character sequances
l = re.findall(pattern, text, re.MULTILINE)
l = [i.capitalize() for i in l] #capitalize() use to make first letter capital
print(l)
```

Output:
```
['Pakistan one of the best contry in the world!', 'Praesent pellentesque mi nec lorem sollicitudin gravida.!']
```

### - Print given pattren or their combination:
* *Example 01*:
```python
text = """We love our country Pakistan Zinda bad!
pakistan one of the best contry in the world!
Hello Wolrd
I'm living in pakistan
"""

pattern = "[pak]+" #it prints all letters that includes either p,a,k or their combination

l = re.findall(pattern, text)
print(l)
```

Output:
```
['ak', 'a', 'a', 'a', 'pak', 'a', 'pak', 'a']
```

=========================================================

* *Example 02*:

```python
text = """We love our country Pakistan Zinda bad!
pakistan one of the best contry in the world!
Hello Wolrd
I'm living in pakistan
"""

# [hwHWI] - is a group of characters
pattern = "^[hwHWI].*" #print letter that starts with either h,w,H,W,I or their combinations
l = re.findall(pattern, text, re.M)
print(l)
```

Output:
```
['We love our country Pakistan Zinda bad!', 'Hello Wolrd', "I'm living in pakistan"]
```
=========================================================

* *Example 03*:
```python
text = """We love our country Pakistan Zinda bad!
pakistan one of the best contry in the world!
Hello Wolrd
I'm living in pakistan
"""

pattern = "^We love.*"
l = re.findall(pattern, text, re.M) + re.findall("^He.*", text, re.M) #print line that starts with 'We' and with 'He'
print(l)
```

Output:
```
['We love our country Pakistan Zinda bad!', 'Hello Wolrd']
```