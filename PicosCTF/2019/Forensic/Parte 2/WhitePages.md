## Descripción

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!

## Pistas

None

## Solución

```python()
1. Se cambia el espacio diferente por 0.
2. Se cambia el espacio normal por 1 
3. sed 's/\xe2\x80\x83/0/g' whitepages.txt | sed 's/\x20/1/g'
4. Después el binario se pasa a ASCCI y así obtenemos la bandera.
```

## Bandera
picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}

## Notas adicionales