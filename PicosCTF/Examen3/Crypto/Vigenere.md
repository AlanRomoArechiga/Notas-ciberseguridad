## Descripción

Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/159/cipher.txt) using this key "CYLAB".

## Pistas

1. [https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher)

## Solución

```python()
1. Descargamos y vemos el mensaje.
2. Como dice el titulo, este reto se trata de `Encripción Vigenere`. Por lo que usando el decodificador online [dcode](https://www.dcode.fr/vigenere-cipher) pude desencriptar facilmente el mensaje utilizando la clave proporcionada.

```

## Bandera

picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_d85729g7}

## Notas adicionales