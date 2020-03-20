# Decimal to Binary

Anki?: NO
Created: Mar 19, 2020 11:01 PM
Github?: NO
Needs review?: 🔴Needs review!
Tags: Algoritmos / EDD

# Links:

[C PROGRAMMING - DECIMAL TO BINARY CONVERSION](https://www.youtube.com/watch?v=fGNwQBAKNds)

# Notes:

## Algoritmo simple - loop & array de largo al azar (C++):

![Decimal%20to%20Binary/Captura_de_pantalla_2020-03-19_a_la(s)_23.00.58.png](Decimal%20to%20Binary/Captura_de_pantalla_2020-03-19_a_la(s)_23.00.58.png)

Para pasar el decimal a binario se implementa una división de decimal original de modo que:

1. Se divide entre 2
2. Se divide hasta que la división entera (int entre int) de cero
3. El binario buscado es el resultado, leído desde el último remainder (el que da división entera igual a 0) hacia el primer remainder.

---

Aquí tenemos las componentes:

`int decimal`  - recibe el input decimal

`int remainder = n%2;` - calculo de resto

`decimal /= 2;` - update de valor inicial para la división

Se sigue hasta que `decimal` sea mayor que 0.

---

Lo que se puede hacer es usar un array `int binary[]`, de modo que este guarde el resto. Ahora, si partimos de `i = 0` hasta el largo de array, obtenemos el binario, pero *al revés.* 

Entonces, para solo printearlo, iremos desde `i-1`  hasta `0`.

Problema: largo de `binary[]` es desconocido, por ende hay que asignarlo al azar.

    void dec2bin(int n){
    	int i = 0;
    	int binary[20]
    	
    	//main loop. guarda el binario en array binary. su orden esta AL REVES!
    	while( n > 0){
    		binary[i] = n % 2;
    		n = n / 2;
    		i++;
    	}
    
    	// printing binary array in reverse order 
        for (int j = i - 1; j >= 0; j--) 
            cout << binaryNum[j]; 
    }

Complejidad: 

while: O(log2n), dado que es la cantidad de dígitos binarios de representación binaria de *n*.

for: O(20), siendo 20 el largo de array. 

Total: O(logn)

## Algoritmo bitwise:

Notar que aritmética de bits es mas rápida que la clásica.

## Algoritmo Stack:

El mismo algoritmo de array, solo que con stack ya el número ya queda "al revés" dado que el stack se escribe de abajo hacia arriba pero se lee de arriba hacia abajo.

Complejidad: 

Total: O(log2n)

## Algoritmo sin array:

[https://www.faceprep.in/c/convert-a-number-from-decimal-to-binary-faceprep/](https://www.faceprep.in/c/convert-a-number-from-decimal-to-binary-faceprep/)
