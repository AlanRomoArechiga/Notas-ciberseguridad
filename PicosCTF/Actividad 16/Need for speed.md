
## Descripción

The name of the game is speed. Are you quick enough to solve this problem and keep it above 50 mph? need-for-speed.

## Pistas

1. What is the final key?

## Solución

```python()
1. Descargamos el programa.
2. Por medio de gdb ejecutamos el código.
3. Con (gdb) set disassembly-flavor intel mostramos la salida del programa en formato intel.
4. Desamblamos la fonción main con el comando disassemble main.
5. Creamos un punto de interrupción con el comando (gdb) break main para poder alterar el funcionamiento del código.
6. Corremos de nuevo el programa con (gdb) run y lo volvemos a desamblar para ver que nos muestra la interrupción.
7. Observamos que en dicha interrupción tenemos las métodos<get_key> y <print_flag>.
8. Mandamos llamar dichos métodos con
(gdb) call (int) get_key() y con (gdb) call (int) print_flag()
9. Obtenemos la bandera

```

## Bandera

PICOCTF{Good job keeping bus #190ca38b speeding along!}

## Notas adicionales