## Descripción

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

## Pistas

1. Try fixing the file header

## Solución

```python()
1. Se utiliza la herramienta pngcheck para analizar las partes que componen a la imagen.
2. Se va reparando cada parte corrupta de la imagen desde el encabezado.
3. Una vez reparada la imagen la podemos visualizar, la cual nos muestra la bandera.

```

## Bandera
picoCTF{C0rruptn_248534}

## Notas adicionales