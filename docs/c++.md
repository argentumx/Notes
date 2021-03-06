- [Operators](#operators)
  * [Ternary](#ternary)
  * [Switch](#switch)
  * [Modulo](#modulo)
- [I/O](#i-o)
  * [Ignorar el input](#ignorar-el-input)
  
***
## Operators
### Ternary
```cpp 
condition : true-value ? false-value;
```

### Switch
En C++, no se permite uso de `float` en `switch` como `switch(valor de un flotante)` dada su imprecisión. `switch` se puede usar solo con valores enteros.

### Modulo
Operador de módulo `%` no se puede usar con números, que no sean enteros. O sea, `double % double`  o ` int % double` es un uso incorrecto. 

Para obtener parte entera de un número en C++ se puede usar `floor()`. Así, la parte decimal de un double será 
`decimal = N - floor(N)`

***
## I/O
### Ignorar el input

Para ignorar el input en C++, se usa `cin.ignore()`.

Si los parentesis se dejan vacios, se ignora el input hasta EOF. De otro manera, se puede pasar dos parametros `cin.ignore(int numero_de_caracteres, char delimitador)` para ignorar los N caracteres hasta un caracter específico.

> As another example, consider:

```cpp
cin.ignore(4,’g’);
cin.get(c);
cout << c << endl;
```
> If the input to this program is “agdfg” then the input is ignored up to and including the ‘g’ so the next character read is ‘d’. The letter “d” is then output.

Para ignorar el input de largo variable hasta un cierto caracter, se puede usar:

```cpp
cin.ignore(numeric_limits<streamsize>::max(), '\n');
```

Donde `numeric_limits<streamsize>::max` proporciona un entero de rango de largo de stream y se ignora hasta el salto de linea.

Asi, podemos recibir el siguiente input para usar solo los numeros en cálculo, obviando el string de nombre de empleado:

Sea input de forma:
- nombre inutil \n
- flotante salario \n
- flotante ventas por mes (15% de bonus al salario) \n

Con

```cpp
cin.ignore(numeric_limits<streamsize>::max(), '\n');
``` 
podemos ignorar esl nombre, sea este de largo 0 a 99999 o millon, ahorrando la memoria.
```cpp
    >joan
    >500.41
    >100
    
    <TOTAL SALARIO = R$ 515.41
```
