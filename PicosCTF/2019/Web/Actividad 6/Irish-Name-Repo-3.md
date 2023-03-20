## Descripción

There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/40742/` ([link](https://jupiter.challenges.picoctf.org/problem/40742/)) or http://jupiter.challenges.picoctf.org:40742. Try to see if you can login as admin!

## Pistas

1. Seems like the password is encrypted.

## Solución

```python()
1. Inpeccionamos el código fuente.
2. Cambiamos el debug a 1 y lo hacemos visible.
3. Ingresamos nuestro payload para la contraseña.
4. Observamos que lo que ingresamos cambia debido a que hay un algoritmo de encriptación.
5. Ingresamos lo encriptado como contraseña para que cuando se aplique el algoritmo de encriptación se deshaga y se quede el texto original.
' or 1 = 1; = ' be 1 = 1;

```

## Bandera

picoCTF{3v3n_m0r3_SQL_4424e7af}

## Notas adicionales