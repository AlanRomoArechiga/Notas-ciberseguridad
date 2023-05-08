## Descripción

The developer of this website mistakenly left an important artifact in the website source, can you find it? The website is here.

## Pistas

1. How could you mirror the website on your local machine so you could use more powerful tools for searching?

## Solución

```python()

1. Para resolver este reto, hacemos caso a la pista dada (duplicar el sitio web). Para poder duplicar el sitio, utilizamos la herramienta de kali `httrack http://saturn.picoctf.net:50303/`. Esto clona exactamente los archivos utilizados en el sitio web en una carpeta con el nombre de la pagina.
2. Inspeccionamos el sitio web y despues de indagar un rato, econtramos que dentro del archivo `style.css` en la carpeta `css`, en la linea 328 vemos con la flag del reto.
```

## Bandera

picoCTF{1nsp3ti0n_0f_w3bpag3s_587d12b8}

## Notas adicionales