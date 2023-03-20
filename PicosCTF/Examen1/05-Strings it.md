## Descripción

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?

## Pistas

[strings](https://linux.die.net/man/1/strings)

## Solución

```bash()
alanarechiga-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}

```

## Bandera
picoCTF{5tRIng5_1T_d66c7bb7}

## Notas adicionales
Grep nos permite buscar la línea que contiene la palabra "pico".