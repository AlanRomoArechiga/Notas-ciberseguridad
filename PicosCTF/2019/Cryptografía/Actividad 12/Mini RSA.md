## Descripción

What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M ** e) is just barely larger than N. Let's decrypt this: [ciphertext](https://mercury.picoctf.net/static/a24cf907007a19dbf30310acad0df9e5/ciphertext)

## Pistas

1. RSA [tutorial](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
2. How could having too small of an `e` affect the security of this key?
3. Make sure you don't lose precision, the numbers are pretty big (besides the `e` value)
4. You shouldn't have to make _too_ many guesses
5. `pico` is in the flag, but not at the beginning

## Solución

```python()
1. Descargamos el archivo.
2. Hacemos un CAT.
3. Con la fórmula r, t = iroot(c, e) en python obtenemos el mensaje.
4. mediante long_to_bytes(r) obtenemos la bandera

```

## Bandera

picoCTF{n33d_a_lArg3r_e_ccaa7776}

## Notas adicionales