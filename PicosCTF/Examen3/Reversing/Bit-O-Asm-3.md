## Descripción

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).

## Pistas

1. -   Not everything in this disassembly listing is optimal.

## Solución

```python()
1. Descargamos y analizamos el código en ensamblador dado.
2. Analizamos las siguientes dos intrucciones dadas, debido a que en ellas se hacen asignaciones de valores:

<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a
<+22>:    mov    DWORD PTR [rbp-0x8],0x4

3. Posteriormente vemos que a `eax` se le asaigna el valor de `rbp-0xc` que es 0x9fe1a.
4. La instruccion `imul eax,DWORD PTR [rbp-0x8]`, se guarda en la variable `eax` el resultado de la multiplicación entre `eax` y `rbp-0x8` que nos da como resultado 0x27f868.
5. Por último, la instruccion `add eax,0x1f5` , se le suma a `eax` el valor de 0x1f5, lo que nos da como resultado `0x27fa5d`, que transformado a decimal seria: 2619997, por lo que únicamente falta formar la bandera con el formato picoCTF{}
```

## Bandera

picoCTF{2619997}

## Notas adicionales