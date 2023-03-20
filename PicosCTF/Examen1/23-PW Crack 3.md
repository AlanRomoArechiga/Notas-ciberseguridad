## Descripción

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Pistas
1. To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
2. To exit `bvi` type `:q` and press enter.
3. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

```python()
1. Descargamos el archivo flag.
2. Ejecutamos mediante python3 el arvhivo descargado.
3. Al pedirnos una contraseña que no conocemos, inspeccionamos el código mediante nano, para de esta manera poder observa qué contraseña se pide, sólo que esta vez hay 7 posibles contraseñas, por lo que hay que interntar con todas.
4. Obteniendo la contraseña, se pide ejecuta nuevamente el código y se pone la contraseña, esto nos devuelve la bandera.

```

## Bandera
picoCTF{m45h_fl1ng1ng_cd6ed2eb}

## Notas adicionales