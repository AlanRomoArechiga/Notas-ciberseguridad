## Descripción

The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.

## Pistas

1. Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.
2. Please use all caps for the message.

## Solución

```python()
1. Vamos al cyberChef.
2. Decodificamos mediante Vigenère decode el texto dado con ayuda de la clave de decifrado.
3. Obtenemos la bandera.
```

## Bandera

picoCTF{CRYPTOISFUN}

## Notas adicionales

https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('SOLVECRYPTO')&input=VUZKS1hRWlFVTkI