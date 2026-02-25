## Descripcion
Find the flag being held on this server to get ahead of the competitionhttp://wily-courier.picoctf.net:64060/
## Solucion

```
En la terminal
curl -s -I http://wily-courier.picoctf.net:64060/index.php
HTTP/1.1 200 OK
Date: Wed, 25 Feb 2026 18:21:45 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8

```
o mediante la extension foxyproxy se cambia el proxy a 127.0.0.1 port 8080
y la herramienta burp suite
entras a http://burp para descargar certificado https
## Notas

## Referencias
