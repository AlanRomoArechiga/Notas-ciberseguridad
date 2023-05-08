## Descripción

Download this image file and find the flag.

## Pistas

1. (None)

## Solución

```python()
1. Para resolver este reto, se nos da el archivo `drawing.flag.svg`, donde su extensión de archivo no es compatible para poder utilizar herramientas de esteganografía. Por lo que procederemos utilizar el comando `cat` ´ para ver si tenemos suerte.
2. Dentro de las dos últimas líneas se nos muestra la bandera pero llena de espacios, por lo que creamos un script en python para eliminar todos los espacios y junar las dos líneas en una sola.

└─$ python3
Python 3.11.2 (main, Feb 12 2023, 00:48:52) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> cadena = "{ 3 n h 4 n c 3 d _ a a b 7 2 9 d d }"
>>> cadena = cadena.replace(' ', '')
>>> print(cadena)
{3nh4nc3d_aab729dd}
```

## Bandera

picoCTF{3nh4nc3d_aab729dd}

## Notas adicionales