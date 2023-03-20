## Descripción

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip)

## Pistas

1. After `unzip` ing, this problem can be solved with 11 button-presses...(mostly Tab)...

## Solución

```python()
1. Se descomprime el archivo .zip con unzip.
2. Con cd entramos en todos los directorios hasta encontrar un archivo ejecutable.
3. Ejecutamos el archivo con ./ y obtenemos la bandera.
```

## Bandera
picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}

## Notas adicionales