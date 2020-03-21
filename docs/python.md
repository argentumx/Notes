    
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
## I/O
### Uso de `map()` en input
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
***
### Ignorar el input
Para ignorar input en python (hasta `\n`), se puede recibirlo con `input()`, pero no asignarlo a ninguna variable.
---

***
## Diccionarios
---
### Uso de `zip()` y la clave entera

En Python es posible crear un diccionario, usando `zip()`:

```python
precios = dict(zip(range(1, 6), [4.00, 4.50, 5.00, 2.00, 1.50]))
```

Crea un diccionaro `precios` de la forma:

`{1: 4.00, 2: 4.50, 3: 5.00, 4: 2.00, 5: 1.50}`
---

***
### Particularidades de función `print()` en manejo de espacios

En Python, los `print()` agregan un espacio extra entre los componentes, de modo que :

```python
print("MODA =", 10)
```
es `MODA = 10` y no `MODA =10`

Nota: En comparacion, C++ no agrega un espacio extra, por lo que siempe es necesario agregarlo manualmente:

```C++
cout << var1 << "\n";
```
---
