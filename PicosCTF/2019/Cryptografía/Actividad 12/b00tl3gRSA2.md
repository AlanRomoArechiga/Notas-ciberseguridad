## Descripción

In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e? Connect with `nc jupiter.challenges.picoctf.org 18243`.

## Pistas

1. What is e generally?

## Solución

```python()
1. Nos conectamos al servidor con nc.
2. Con los datos dados aplicamos la fórmula m = pow(c,e,n).
3. Obtenemos 180638594769037903267909311328535969949661653466129492033745533
4. Pasamos eso a texto mediante long_to_bytes(m)
5. Obtenemos la bandera.

```

## Bandera

picoCTF{bad_1d3a5_4783252}

## Notas adicionales