## Objetivo

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso

**bandit.labs.overthewire.org**

**bandit**8

TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Solución

```bash()
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

```

## Notas adicionales

Para poder imprimir lienas unicas, primero se deben ordenar para poder compararlas. **sort**: Ordenar líneas de archivos de texto **uniq** : informar u omitir líneas repetidas **-u**: solo imprime líneas únicas.

## Referencias

https://david-varghese.medium.com/overthewire-bandit-level-8-level-9-b0a860b1c243