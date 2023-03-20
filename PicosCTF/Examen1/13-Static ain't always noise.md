## Descripción

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static)? This [BASH script](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh) might help!

## Pistas

1. None

## Solución

```python()
1. Descargar los archivos y darles permiso de ejecución.
2. ./ltdis.sh static 
3. cat static.ltdis.strings.txt | grep pico
```

## Bandera
picoCTF{d15a5m_t34s3r_6f8c8200}

## Notas adicionales