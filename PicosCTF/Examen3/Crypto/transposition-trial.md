## Descripción

Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/192/message.txt).

## Pistas

1. Split the message up into blocks of 3 and see how the first block is scrambled

## Solución

```python()
1. Descargamos el texto dado.
2. Observamos que se nos da la bandera pero codificada de la siguiente manera:
 `heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2`.
3. Como nos dice la descripcion, en un grupo de 3 caracteres (incluyendo el espacio), se pondrá el ultimo char al principio y se recorreran los primeros dos un espacio.
4. Para optimizar lo anterior, se crea el siguiente script en python:

c = "`heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2"
cList = list(c)
nList = []
flag = ""
for i, char in enumerate(cList):
    if ((i + 1) % 3 == 0):
        nList.append(cList[i])
        nList.append(cList[i-2])
        nList.append(cList[i-1])
        
for char in nList:
    flag += char

print(flag)

5. Obtenemos como salida:
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}
```

## Bandera

picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}

## Notas adicionales