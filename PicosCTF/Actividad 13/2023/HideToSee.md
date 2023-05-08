## Descripción

How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/237/atbash.jpg).

## Pistas

1. 1.  Download the image and try to extract it.

## Solución

```bash()
┌──(kali㉿kali)-[~/picoCTF-2023/Cryptography/HideToSee]
└─$ ls
atbash.jpg
┌──(kali㉿kali)-[~/picoCTF-2023/Cryptography/HideToSee]
└─$ steghide info atbash.jpg                     
"atbash.jpg":
  formato: jpeg
  capacidad: 2.4 KB
�Intenta informarse sobre los datos adjuntos? (s/n) s
Anotar salvoconducto: 
  archivo adjunto "encrypted.txt":
    tama�o: 31.0 Byte
    encriptado: rijndael-128, cbc
    compactado: si
┌──(kali㉿kali)-[~/picoCTF-2023/Cryptography/HideToSee]
└─$ steghide extract -sf atbash.jpg -xf datos.txt
Anotar salvoconducto: 
anot� los datos extra�dos e/"datos.txt".

┌──(kali㉿kali)-[~/picoCTF-2023/Cryptography/HideToSee]
└─$ cat datos.txt 
krxlXGU{zgyzhs_xizxp_05y2z65z}

┌──(kali㉿kali)-[~/picoCTF-2023/Cryptography/HideToSee]
└─$

```

## Bandera

picoCTF{atbash_crack_05b2a65a}

## Notas adicionales