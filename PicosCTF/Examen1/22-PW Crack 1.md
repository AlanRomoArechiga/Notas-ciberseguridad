## Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

## Pistas

1. To view the file in the webshell, do: `$ nano level1.py`
2. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
3. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

```python()
1. Descargamos el archivo flag.
2. Ejecutamos mediante python3 el arvhivo descargado.
3. Al pedirnos una contraseña que no conocemos, inspeccionamos el código mediante nano, para de esta manera poder observa qué contraseña se pide.
4. Obteniendo la contraseña, se pide ejecuta nuevamente el código y se pone la contraseña, esto nos devuelve la bandera.

```

## Bandera
picoCTF{545h_r1ng1ng_fa343060}

## Notas adicionales