## Descripción

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:34561/](http://mercury.picoctf.net:34561/)

## Pistas

1. Maybe you have more than 2 choices.
2. Check out tools like Burpsuite to modify your requests and look at the responses.

## Solución

```python()
curl -I http://mercury.picoctf.net:34561/index.php 


```

## Bandera

picoCTF{r3j3ct_th3_du4l1ty_8f878508}

## Notas adicionales

El comando curl -I equivale a usar curl -X HEAD
El comando curl -X método nos permite indicar qué método queremos usar para realizar la consulta.