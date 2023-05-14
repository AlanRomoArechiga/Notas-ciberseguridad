## Descripción

We have recovered a binary and a text file. Can you reverse the flag.

## Pistas

1. objdump and Gihdra are some tools that could assist with this

## Solución

```python()
1. Analizamos el ejecutable dado por medio de objdump.
2. Al ver que la información no es de tanta relevancia, procedemos a abrir el archivo por medio de Gihdra el cual nos muestra el main copilado.
3. Nos centramos en la parte que codifica la bandera.
4. Creamos un archivo en python para decodificar dicha bandera.

cifrado = "picoCTF{w1{1wq8/7376j.:} "
flag = ""

for i in range(8,len(cifrado)-1):
    if i & 1 == 0:
      flag += chr(ord(cifrado[i]) -5)
    else:
        flag += chr(ord(cifrado[i]) + 2)
print(flag)

5. Obtenemos la bandera.

```

## Bandera

picoCTF{r3v3rs312528e05}

## Notas adicionales