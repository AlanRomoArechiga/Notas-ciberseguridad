## Descripción

Download the packet capture file and use packet analysis software to find the flag.

## Pistas

1. Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.

## Solución

```python()
1. Analizamos el paquete dado con Wireshark
2. Damos click derecho a un paquete TCP, le damos en `follow` -> `TCP stream`, donde podremos ver la flag:

```

## Bandera

picoCTF{p4ck37_5h4rk_b9d53765}

## Notas adicionales