## Descripción

onnect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 60602 -U postgres pico`Password is `postgres`

## Pistas

1. What does a SQL database contain?

## Solución

```python()
1. Para resolver este reto, ingresamos a la base de datos que se nos proporciona.
2. Estando ya dentro, lo primero que tenemos que hacer es ver que tablas existen en la base de datos, para poder asi ingresar a ellas y ver su contenido. Como estamos en psotgreSQL, el comando que utilizaremos para esto es `\dt`.
3. Sabiendo que el nombre de la tabla es `flags`, utilizaremos la sentencia `select * from flags;` para poder ver todo el contenido de la tabla, en la cual entramos el valor de la bandera.

```

## Bandera

picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}

## Notas adicionales