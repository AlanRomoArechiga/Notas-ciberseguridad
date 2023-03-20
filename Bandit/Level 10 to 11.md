## Objetivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.

## Datos de acceso

bandit10    
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solución

```bash()
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ 
```

## Notas adicionales

**Base64**: codificar o decodificar ARCHIVO, o entrada estándar, a salida estándar. **-d, --decode**: decodifica los datos

## Referencias

https://www.gnu.org/software/coreutils/manual/html_node/base64-invocation.html#base64-invocation