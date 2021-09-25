# Types of Inheritance

## Multilevel Inheritance

```python
class A:
    a = 1
class B(A):
    b = 2
class C(B):
    c = 3
print(C.a)
```

## Multiple Inheritance

```python
class A:
    a = 1
class B:
    a = 2
    b = 2
class C(A,B):
    c = 3
# print(C.a)
```

## Hierchial Inheritance

```python
class A:
    a = 1
class B(A):
    b = 2
class C(A):
    c = 3
# print(A.a)
```

## Hybrid Inheritance

```python
class A:
    a = 1
class B(A):
    b = 2
class C(A):
    c = 3
class D(C):
    d = 4

print(A.a)
print(D.a)
```

