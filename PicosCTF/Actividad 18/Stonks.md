## Descripción

I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/7e71fc0d8cc3339bfad6bf408f7dc510/vuln.c) `nc mercury.picoctf.net 6989`

## Pistas

1. -   Okay, maybe I'd believe you if you find my API key.

## Solución

```python()
1. Observamos el código.
2. Rastreamos la ejecución a través de la primera opción, con lo cual detectamos un bloque dentro de la función  `buy_stonks()`:
```

```bash()
char *user_buf = malloc(300 + 1); printf("What is your API token?\n"); scanf("%300s", user_buf); printf("Buying stonks with token:\n"); printf(user_buf);
```


```python()
3. Viendo de cerca el comienzo de la función `buy_stonks()`, observamos lo que parece ser el archivo de bandera que se carga y su contenido se copia en un búfer en la pila.
4. Se nos muestra lo que parece ser un código ASCII comenzando en el lugar 15.  Copiamos todo desde el primer bloque de bytes ASCII hasta el bloque que contiene un byte nulo.
5. Realizamos un script en python para decodificar la bandera:

from binascii import unhexlify

flag = b"".join(
    [
        unhexlify("6f636970")[::-1],
        unhexlify("7b465443")[::-1],
        unhexlify("306c5f49")[::-1],
        unhexlify("345f7435")[::-1],
        unhexlify("6d5f6c6c")[::-1],
        unhexlify("306d5f79")[::-1],
        unhexlify("5f79336e")[::-1],
        unhexlify("35386130")[::-1],
        unhexlify("32356533")[::-1],
        unhexlify("007d")[::-1],
    ]
).decode()

print(flag)

6. Obtenemos la bandera.

```


## Bandera

picoCTF{I_l05t_4ll_my_m0n3y_6045d60d}

## Notas adicionales