## Descripción

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/2604f8b51a5cc62d38a3736938f19cef/values)

## [](https://github.com/DarthTrinity/Notas-Hacking/blob/main/picoCTF%202021/Criptography/Mind%20your%20Ps%20and%20Qs.md#pistas)

## Pistas

1. -   Bits are expensive, I used only a little bit over 100 to save money

## [](https://github.com/DarthTrinity/Notas-Hacking/blob/main/picoCTF%202021/Criptography/Mind%20your%20Ps%20and%20Qs.md#soluci%C3%B3n)

## Solución

```python()
1. Descargamos el archivo.
2. En base a las variables dadas obtenemos:
3. Para poder obtener el texto plano, necesitamos de las variables p y q, para asi poder obtener tn y despues d y poder sustituirlos en las formula que nos da el texto plano: m = c^d mod n. Para poder obtener estas variables, utilizaremos Factordb 
4. Sabiendo esto, podemos sustituir los valores para obtener el valor de tn y d y asi sustituir todas estas variables en la formula para obtener el texto plano. Para eso cree un programa en python que nos diera la bandera sabiendo todo esto.
```

## Bandera

picoCTF{sma11_N_n0_g0od_13686679}

## Notas adicionales