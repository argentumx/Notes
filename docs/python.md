    
***

### Ternary
Usando un diccionario:

```python 
print({True: a, False: b} [a < b])
```

Usando una tupla:

```python
print( (b, a) [a < b] )
```

La manera más eficiente es usar una expresión lambda, dado que la expresión condicional se evalua solo una vez, en vez de 2, como en caso de la tupla o el diccionario:

    
```python
print((lambda: b, lambda: a)[a < b]())
```
***
