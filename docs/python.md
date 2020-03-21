    
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

### Uso de map() en input
En Python, para recibir input de tipo

```
3.0 4.0 5.0
```

Tenemos que usar `map()`:

```python
a, b, c = map(float, input().split())
```

Nota: En C++, en cambio, basta con cin:

```C++
double a, b, c;
cin >> a >> b >> c;
```
