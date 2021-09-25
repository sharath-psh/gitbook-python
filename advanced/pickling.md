# Pickling

* Pickling helps us in transfering data.
* Python pickle module helps us to convert data\(variables,string,etc\) to data file.
* This data file is stream of bytes.\(1,0\)
* This convertion of data to bytestream is called as 'Serialization'. And converting

  bytestream back to data is called as 'Deserialization'

## convert data to pickle

```python
import pickle
li = [1,2,3,4]
with open('test.data','wb') as fo:
    pickle.dump(li,fo)
```

## convert pickle to data

```python
pickle_off = open ("test.data", "rb")
emp = pickle.load(pickle_off)
print(emp)
```

