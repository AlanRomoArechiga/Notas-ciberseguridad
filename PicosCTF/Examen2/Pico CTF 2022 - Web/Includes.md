## Descripción

Can you get the flag?Go to this [website](http://saturn.picoctf.net:56469/) and see what you can discover.

## Pistas

1. Is there more code than what the inspector initially shows?

## Solución

```python()
1.Para resolver este reto, debemos entrar a la inspección del elemento, y analizando la pista, nos da a entender que la pagina tiene varios archivos.
2. Revisando el apartado `sources` encontramos 3 archivos diferentes (html, js y css). Inspeccionando cada uno de ellos podemos ver que en el archivo `script.js` encontramos una parte de la flag.
3. Revisando el archivo `style.css` encontramos la parte faltante.
```

## Bandera

picoCTF{1nclu51v17y_1of2_f7w_2of2_b8f4b022}

## Notas adicionales