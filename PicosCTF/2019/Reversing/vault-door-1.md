## Descripción

This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/ff2585f7afd21b81f69d2fbe37c081ae/VaultDoor1.java)

## Pistas

1. Look up the charAt() method online.

## Solución

```python()
1. Descargamos el código.
2. Inspeccionamos el código.
3. Sacamos la función que hace la validación del password y todas las posiciones las poneamos a dos dígitos para poder ordenar la posición de cada caracter por número.
4. Con el comando cat bandera1 | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n" obtenemos la contraseña.
5. Ejecutamos el código y ponemos la contraseña obtenida para comprobar. 
```

## Bandera

picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_75092e}

## Notas adicionales