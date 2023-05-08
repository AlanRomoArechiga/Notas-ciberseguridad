## Descripción

We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:65352/).

## Pistas

1. folders folders folders

## Solución

```python()
1. Si hacemos clic con el botón derecho + inspeccionar y vemos la pestaña de fuentes, encontramos que algunos de los archivos están en una carpeta llamada "secret".
2. Navegamos al suburl secret ([http://saturn.picoctf.net:54925/secret/](http://saturn.picoctf.net:54925/secret/)), encontramos un sitio web que dice "Finalmente. Casi me encontraste. Lo estás haciendo bien". Vamos por buen camino.
3. Repetimos el mismo proceso que antes, encontramos que hay otra carpeta por nombre "hidden", por lo que navegamos a [http://saturn.picoctf.net:54925/secret/hidden/](http://saturn.picoctf.net:54925/secret/hidden/).
4. Seguimos repitiendo este proceso hasta que llegamos a un sitio web que dice "Finalmente. Me encontraste. Pero puedes verme".

```

## Bandera

picoCTF{succ3ss_@h3n1c@10n_790d2615}

## Notas adicionales