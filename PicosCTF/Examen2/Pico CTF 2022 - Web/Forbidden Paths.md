## Descripción

Can you get the flag? Here's the website. We know that the website files live in /usr/share/nginx/html/ and the flag is at /flag.txt but the website is filtering absolute file paths. Can you get past the filter to read the flag?

## Pistas

1. (None)

## Solución

```python()
1. Para solucionar este reto, no funciona utilizar `file paths` por lo que poner `../../../../flag.txt` desde el navegador no servira de nada, ya que nos da un error.
2. Viendo los archivos a los que se podemos acceder, podemos ver que solo se escrribe en el input de la pagina para poder obtener su contenido.
3. Por lo que entonces es mas logico escribir `../../../../flag.txt` en el input de la pagina, lo que nos dara la flag.

```

## Bandera

picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}

## Notas adicionales