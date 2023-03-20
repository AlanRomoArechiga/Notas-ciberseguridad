## Objetivo

The password for the next level is stored **somewhere on the server** and has all of the following properties:

## Datos de acceso

**bandit.labs.overthewire.org**

**bandit6**

P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Solución

```bash()
bandit6@bandit:~$ ls
bandit6@bandit:~$ find /  -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```

## Notas adicionales

**2>/dev/null** elimina los mensaje de "Permiso denegado" El comando **find** nos ayuda a buscar cualquier archivo, donde se pueden especificar propiedades especificas, como: **/**: El diagonal se utiliza por que buscamos la ruta donde se encuentra el archivo, ya que no tenemos mas información **-user**: El usuario al que pertenece **-group**: el grupo al que pertenece **-size**: especifica el tamaño del archivo.

## Referencias

https://medium.com/@theGirlWhoEncrypts/overthewire-bandit-level-6-level-7-e1930ac68a54