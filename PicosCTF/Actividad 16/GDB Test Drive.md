## Descripción

Can you get the flag? Download this binary. Here's the test drive instructions:

```
$ chmod +x gdbme
$ gdb gdbme
(gdb) layout asm
(gdb) break *(main+99)
(gdb) run
(gdb) jump *(main+104)
```

## Pistas

+ None

## Solución

```python()
1. Ejecutemos el binario en gdb y desmontemos layout asm.
2. Al ejecutar este binario, no proporciona nada. Una vez desmontado esta función principal. La parte de ejecución se ha ido a dormir. Es por eso que dividimos la dirección principal en *(main+99) y saltamos a la dirección *(main+104) para obtener la bandera.

```

## Bandera

picoCTF{d3bugg3r_dr1v3_197c378a}

## Notas adicionales
