## Descripcion
How about we take you on an adventure on exploring certificate signing requestsTake a look at this CSR file [here](https://artifacts.picoctf.net/c/423/readmycert.csr).
## Solucion
picoCTF{read_mycert_57f58832}
## Notas
```
openssl req -in readmycert.csr -noout -text
```
## Referencias

[ReadMyCert — PicoCTF Writeup. Day 26 | by Eric H | Medium](https://medium.com/@erichdryn/readmycert-picoctf-writeup-a82c993a1007)