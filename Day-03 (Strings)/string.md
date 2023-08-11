# String
String is a collection of alphabets, words or other characters. It is a sequence of characters. 

String can be written using "double quote" or using 'single quote'.

## Prove That:
Prove that, a certain set of characters is string.
 
**Using double quote**

```python
data = "Python Language" 
print(data)
print(type(data))   #channing rule
```

Output:
```markup
Python Language
<class 'str'>
```
 
**Using single quote**

```python
data = 'Python Language' 
print(data)
print(type(data))   #channing rule
```

Output:
```markup
Python Language
<class 'str'>
```

## Examples

#### 1. Using 'double quote' between single quoted string:

```python
data = 'Python Language "Hello world' 
print(data)
print(type(data))  
```

Output:
```markup
Python Language "Hello world
<class 'str'>
```

#### 2. Using 'single quote' between double quoted string:

```python
data = "Python Language 'Hello world"
print(data)
print(type(data))  
```

Output:
```markup
Python Language 'Hello world
<class 'str'>
```

#### 3. Use of ' \ '

Backslash - use to convert special character into normal character. 

**Example#1**

```python
data = 'Python Language\ 123 "Hello world"'
print(data)
print(type(data))  
```

Output:
```markup
Python Language 'Hello world
<class 'str'>
```
___

**Example#2**

```python
a = '"Python\'s awesome" She said'
print(a)
print(type(a))  
```

Output:
```markup
"Python's awesome" She said
<class 'str'>
```

## Multiline String:
A multiline string in Python begins and ends with either three single quotes or three double quotes. 

Any quotes, tabs, or newlines in between the “triple quotes” are considered part of the string.

**Example#1**

```python
a = "Line1 python"\ 
"Line2 python"\
"Line3 python"
print(a) #here '\' shows that line is continue
print(type(a))
```

Output:
```markup
Line1 pythonLine2 pythonLine3 python
<class 'str'>
```
___

**Example #2**

```python
b = """Line1 python
Line2 python
Line3 python """ 
print(b) #triple double quote
print(type(b))
```

Output:
```markup
Line1 python
Line2 python
Line3 python
<class 'str'>
```

## Key Points:
* \t - use to create 4spaces in string.
* \n - use to add new line in string.
* Triple single quotes or Triple double quotes are the boundaries of a string. 