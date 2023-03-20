## Descripción

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm) has extraordinarily helpful information...

## Pistas

1. This program will only work in the webshell or another Linux computer.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm`
3. Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`

## Solución

```python()
1. wget https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm
2. chmod +x warm`
3. ./warm -h
```

## Bandera
picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}

## Notas adicionales