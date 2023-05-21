## Descripción

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).

## Pistas

1. PTR`'s or 'pointers', reference a location in memory where values can be stored.

## Solución

```python()
1. Descargamos y analizamos las instrucciones que este contiene.
2. Analizando cada instrucción, encontramos la siguiente:
<+15>: mov DWORD PTR [rbp-0x4],0x9fe1a Esta instrucción mueve el valor inmediato 0x9fe1a (hexadecimal) a la ubicación de memoria apuntada por rbp-0x4.
3. Como podemos ver, se nos dice que se mueve a la variable `eax` el valor de laubicación de memoria apuntada por rbp-0x4. el cual seria `0x9fe1a`, que en deciamal es: 654874, por lo que la bandera es: picoCTF{654874}

```

## Bandera

picoCTF{654874}

## Notas adicionales