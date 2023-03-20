## Descripción

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210

## Pistas

1. What is that cookie?
2. Have you heard of JWT?

## Solución

```python()
Para esta solución hay que cambiar la cookie para que nos reconozca como admins, para esto se usa el cookie editor y jwt.io, únicamente cambiamos el nombre de usuario por admin y cambiamos la palabra clave con la que se codifica el jwt.
Para obtener la palabra clave utilizamos la herramienta jhon en linux mediante el comando jhon nombreArchivoConLaCookie -w=/usr/share/wordlists/rockyou.txt
```

## Bandera
picoCTF{jawt_was_just_what_you_thought_44c752f5}

## Notas adicionales