## Descripción

The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796

## Pistas

1. Hmm it doesn't seem to check anyone's password, except for Joe's?

## Solución

```python()
Para esta solución se tiene que inspeccionar la cookie al ingresar y en el apartado de admin cambiar el valor de false a true y simplemente recargar la página para que se nos muestre la cookie.

```

## Bandera
picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}

## Notas adicionales