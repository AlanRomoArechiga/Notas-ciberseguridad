## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Pistas

1.  None

## Solución

```python()
1. Se abre el archivo.
2. Se filtran los paquetes con: udp.dstport==22
3. Por medio de la librería scapy hacemos un programa en python el cual nos permitirá realizar un bucle para ir decodificando a ASCCI todos los valores que va obteniendo, para de esta manera formar una cadena con todos estos códigos, los cuales conforman la bandera.
```

## Bandera

picoCTF{p1LLf3r3d_data_v1a_st3g0}

## Notas adicionales