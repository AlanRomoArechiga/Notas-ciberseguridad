## Descripción

This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/c695ee23309d453a3ef369c34cc1bccb/VaultDoor4.java)

## Pistas

1. Use a search engine to find an "ASCII table".
2. You will also need to know the difference between octal, decimal, and hexadecimal numbers.

## Solución

```python()

4. 1. Descargamos el archivo.
2. Observamos que la función que verifica la contraseña tiene la contraseña en base 10, base octal y base hexadecimal.
3. Con la función String.fromCharCode() en javaScript obtenemos la contraseña en carateres.
4. Sumamos la parte ya decodificada con la que nos devolvió la función String.fromCharCode()
```

## Bandera

picoCTF{jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b}

## Notas adicionales