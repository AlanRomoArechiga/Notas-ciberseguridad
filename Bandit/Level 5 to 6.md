## Objetivo

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

## Datos de acceso

**bandit5**

lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## Solución

```bash()
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

```

## Notas adicionales

El comando **find** nos ayuda a buscar cualquier archivo, donde se pueden especificar propiedades especificas, como: **.**: el punto esta por que se busca un archivo **-readable**: que pueda ser apto para leerse **-type**: especifica el tipo de archivo **-size**: especifica el tamaño del archivo

## Referencias