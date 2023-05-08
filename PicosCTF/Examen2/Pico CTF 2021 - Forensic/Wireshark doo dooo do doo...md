## Descripción

Can you find the flag? shark1.pcapng.

## Pistas

1. (None)

## Solución

```python()
1. Para resolver este reto, se nos da un archivo de paquetes de red, y como dice el nombre del reto, utilizaremos `Wireshark`.
2. Para empezar, analizaremos los diferentes streams de los paquetes TCP, ya que en general, ahi encontramos la flag.
3. Al llegar al stream 5, encontramos la flag codificada en ROT13.
4. Con ayuda de Cyberchef decodificamos y obtenemos la bandera. 

```

## Bandera

picoCTF{p33kab00_1_s33_u_deadbeef}

## Notas adicionales
