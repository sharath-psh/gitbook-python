# File Handling

Using python we are able to read, write or update contents to the file

* open\(\) function helps us to create a file object.
* this file object helps us to access the file.
* read\(\) helps us to read the file.

File handling modes: "r" - Read - Default value. Opens a file for reading, error if the file does not exist "a" - Append - Opens a file for appending, creates the file if it does not exist "w" - Write - Opens a file for writing, creates the file if it does not exist "x" - Create - Creates the specified file, returns an error if the file exists

Syntax: \(to create file object\)

> file\_obj\_name = open\('file\_name','mode'\)

## To read a file

```python
fo = open('sample.txt','r')
print(fo.read())
```

## Create a file

```python
fo = open('f2.txt','x')
```

* creating file with same file name will result in error

## Read the file line by line

```python
f = open('sample.txt','r')
for i in f:
    print(i)
f.close()
```

## Read the file and store it in a list

```python
fo = open('sample.txt','r')
li = fo.readlines()
print(type(li))
print(li)
```

## Writing to the file

```python
fo = open('f2.txt','w')
fo.write('text22222')
fo.close()
```

```python
fo = open('sample.txt','r')
print(fo.read())
fo.close()
```

* write mode replaces the entire contents of the file.\(overwriting\)
* file is created if it does not exist
* in order to read from the file again, we use the 'r' mode.

## Appending contents to the file

```python
fo = open('sample.txt','a')
li = ['hello', 'how', 'are', 'you']
for i in li:
    fo.write('\n'+i)
fo.close()
```

## alternative method to open a file using 'with'

```python
fo = open('sample.txt','r')
print(fo.read())
fo.close

with open('sample.txt','r') as fo:
    print(fo.read())
```

* with does not require closing the file

## alternative method to open a file using 'with'

```python
fo = open('sample.txt','r')
print(fo.read())
fo.close

with open('sample.txt','r') as fo:
    print(fo.read())
```

* with does not require closing the file

