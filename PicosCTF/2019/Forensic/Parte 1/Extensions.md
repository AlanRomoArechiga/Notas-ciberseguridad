
## Descripción

This is a really weird text file TXT? Can you find the flag?

## Pistas

-   How do operating systems know what kind of file it is? (It's not just the ending!
-   Make sure to submit the flag as picoCTF{XXXXX}

## Solución

```python()
1. Para resolver el reto las pistas son importantes, ya que nos habla de las extensiones de un archivo.
2. Como el archivo dado es .txt lo primero que hice fue usar el comando cat, pero al mostrar carácteres extraños pase a usar el comando strings pero siguio sin dar algun resultado.
3. Gracias a las pistas, me dio curiosidad ver los metadatos del archivo para ver si en realidad es un archivo .txt, pero los datos decian que era un archivo .png, por lo que con el comando mv le cambie el nombre de la extensión.
```

## Bandera

picoCTF{now_you_know_about_extensions}

## Notas adicionales