## Descripción

Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `a13b7f9d`

## Pistas

1. Finding a cheatsheet for bash would be really helpful!

## Solución

```python()
1. Nos conectamos al servidor.
2. Por medio de cat leemos la primera parte de la bandera.
3. Con cd .. nos movemos al directorio anterior y encontramo la segunda parte.
4. Con cd .. nos movemos al directorio raiz y encontramos la tercera parte de la bandera.
5. Unimos todas las partes para crear la bandera.
```

## Bandera
picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}

## Notas adicionales