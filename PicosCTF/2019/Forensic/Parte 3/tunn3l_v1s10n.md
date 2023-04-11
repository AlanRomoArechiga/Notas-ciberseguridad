## Descripción

We found this file. Recover the flag.

## Pistas

1. Weird that it won't display right...

## Solución

```python()
1. Para resolver este reto, el primer paso fue cambiarle el nombre del archivo tunn3l_v1s10n a tunn3l_v1s10n.bmp, ya que le faltaba la extension al archivo. Esto se puede comprobar tambien con el comando exiftool.

2. Como la imagen no se puede abrir, iremos a la herramienta HxD para ver su composicion en hexadecimal. Analizandola, vemos que tiene varios fallos en su cabecera.

3. Despues de corregir esto, ya podemos abrir la imagen, pero esta incompleta, por lo que ahora tenemos que modificar el tamaño para obtener la imagencompleta.

4. Despues de modificar esto, podremos ver la bandera hasta arriba de la imagen:

```

## Bandera

picoCTF{qu1t3_a_v13w_2020}

## Notas adicionales