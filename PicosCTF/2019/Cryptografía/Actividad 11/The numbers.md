## Descripción

The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?

## Pistas

1. The flag is in the format PICOCTF{}

## Solución

```python()
1. Se descarga la imagen.
2. Ingresamos a cyberChef.
3. Escribimos los números de la imagen dentro del cyberChef y lo decodificamos con A1Z26 Cipher Decode.
4. Esto nos devuelve la bandera decifrada

```

## Bandera

picoCTF{thenumbersmason}

## Notas adicionales

https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=JyBvciAxID0gMTs