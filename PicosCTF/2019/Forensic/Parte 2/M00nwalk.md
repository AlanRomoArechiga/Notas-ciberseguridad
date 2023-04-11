## Descripción

Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.

## Pistas

-   How did pictures from the moon landing get sent back to Earth?
-   What is the CMU mascot?, that might help select a RX option

## Solución

```python()

1. Este [tutorial](https://ourcodeworld.com/articles/read/956/how-to-convert-decode-a-slow-scan-television-transmissions-sstv-audio-file-to-images-using-qsstv-in-ubuntu-18-04) explica cómo usar un programa llamado qsstv para convertir los archivos de audio a imágenes. 
2 
. La pista preguntaba "¿Cuál es la mascota de CMU?" - la respuesta es "Scotty the Scottie Dog". Esto insinuó que deberíamos seleccionar "Scottie 1" como "Modo" de QSSTV. También tuve que seleccionar "Auto Slant" a través de prueba y error.
3. En este punto, podemos hacer clic en el botón "Reproducir" en QSSTV para iniciar el receptor y luego reproducir el archivo de audio:
```
└─$ paplay -d virtual-cable message.wav  
```
4. La imagen es recibida y decodificada por el programa:

```

## Bandera

picoCTF{beep_boop_im_in_space}

## Notas adicionales