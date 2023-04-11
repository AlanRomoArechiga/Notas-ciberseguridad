## Descripción

We found this packet capture and key. Recover the flag.

## Pistas

-   Try using a tool like Wireshark.
-   How can you decrypt the TLS stream?

## Solución

```python()
1. Para resolver este reto, se nos da un archivo capture-pcap que abriremos con wireshark y un archivo picopico.key que nos ayudara despues con el reto.
2. El primer paso para resolver este reto es seguir el flujo de TCP, y nos muestra que los datos están encriptados (excepto algunas partes durante el protocolo de enlace, como el certificado)
3. Si inspeccionamos ese handshake de manos, más precisamente, observando el paquete Server Hello, vemos que se seleccionó un conjunto de cifrado que se basa en RSA y AES.
4. Wireshark puede descifrar los datos cifrados con este conjunto de cifrado cuando proporcionamos la clave RSA privada del servidor. Esto se debe a que, en este ejemplo, Wireshark necesita descifrar el secreto premaestro enviado por el cliente al servidor. Este secreto maestro previo se cifra con la clave RSA pública del servidor. Por lo que aqui es donde el archivo picopico.key nos caera de perlas.
5. Para poder agregar esta clave, iremos a edit/preferences, despues seleccionaremos el protocolo TLS y editaremos la RSA Keys list agregandole el arhcivo que contiene la clave.
6. Cuando cierre los cuadros de diálogo y la pantalla principal recupere el foco, los datos TLS se descifrarán.
7. Cuando seleccionamos TCP, todavía tenemos datos encriptados, pero cuando seleccionamos TLS, ahora podemos ver los datos descifrados:

```

## Bandera

picoCTF{nongshim.shrimp.crackers}

## Notas adicionales