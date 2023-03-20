## Descripción

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

## Pistas

1. Does that encoding look familiar?
2. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

```python()
1. Descargamos el archivo flag.
2. Ejecutamos mediante python3 el arvhivo descargado.
3. Al pedirnos una contraseña que no conocemos, inspeccionamos el código mediante nano, para de esta manera poder observa qué contraseña se pide, sólo que esta vez la contraseña está en hexadecimal, por lo que hay que pasarla a ASCCI primero.
4. Obteniendo la contraseña, se pide ejecuta nuevamente el código y se pone la contraseña, esto nos devuelve la bandera.

```

## Bandera
picoCTF{tr45h_51ng1ng_489dea9a}

## Notas adicionales