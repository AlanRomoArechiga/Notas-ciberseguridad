## Descripción

The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:61304/) out.

## Pistas

1. None

## Solución

```python()
1. Para resolver este reto, el nombre y la descripción nos dan dos pistas importantes. La descripción nos dice que la flag no esta en el sitio web, y el nombre nos da un indicio sobre algo que ya conocemos: `/robots.txt`.
2. Los datos dados por este archvio son:

User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

3. Observamos que la línea que contiene anMvbXlmaWxlLnR4dA== está codificada en base64. Esto lo observamos gracias al '=='
4. Decodificamos esta línea, lo cual nos da lo siguiente:
	js/myfile.txt
5. Ingresamos a esta parte del sitio web y ahí encontramos la bandera.

```

## Bandera

picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}

## Notas adicionales