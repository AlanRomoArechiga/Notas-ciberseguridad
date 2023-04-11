
## Descripción

We found this packet capture. Recover the flag.

## Pistas

-   Try using a tool like Wireshark
-   What are streams?

## Solución

```python()
1. Para obtener la solución a este reto, necesitamos abrir el archivo desde wireshark, donde encontraremos una captura de peticiones.
2. Para obtener la respuesta, analizamos una por una el codigo hexadecimal transformado a ASCII en las peticiones para ver si encontrabamos algo interesante.
3. Despues de un rato, vimos que en el protocolo UDP aparcia constantemete "pico" por lo que lo filtre ene l buscador.
4. Despues de analizar una por una en las peticiones filtradas, se empieza a ver que la flag esta descompuesta en caracacteres, donde todos estaban destinados a una sola direccion ip.
5. Por lo que dandole click derecho a una de esas peticiones e ir a follow - UDP streams, me mostro la flag completa.

```

## Bandera
picoCTF{StaT31355_636f6e6e}

## Notas adicionales