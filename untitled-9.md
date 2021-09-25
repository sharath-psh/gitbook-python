# JSON

## Converting from JSON to python

```python
import json
j = '{"a":1,"b":2,"c":3}'
jo = json.loads(j)
print(jo["a"])
print(type(jo))

for i in jo:
    print(jo[i],i)
```

## Converting Python dict to JSON

```python
import json
di = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

jj = json.dumps(x)
print(jj)
```

