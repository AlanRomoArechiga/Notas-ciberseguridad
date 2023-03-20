## Objetivo

The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso

**bandit.labs.overthewire.org**

**bandit1**

NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## Solución

```bash()
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ exit
```

## Notas adicionales
Como no se puede acceder directamente a '-', busque la ruta actual y sumandole el directorio encontrado con ls, lei directamente lo ue esta adentro de la ruta.
## Referencias
https://www.webservertalk.com/dashed-filename#:~:text=In%20some%20cases%2C%20you%20may,starts%20with%20a%20dash%20(%2D).