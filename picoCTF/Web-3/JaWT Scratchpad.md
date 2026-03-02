## Descripcion
Check the admin scratchpad!http://fickle-tempest.picoctf.net:50322
## Solucion
Nos logueamos con cualquier usuario
Copiamos el token jwt a un archivo llamado token
Lo crackeamos en kali usando john con el diccionario rockyou.txt

`gizip -d /usr/share/wordlists/rockyou.txt.gz john token -w=/usr/share/wordlists/rockyou.txt`

Vamos al sitio jwt debuger, y modificamos el payload por admin
Ponemos la palabra crackeada en la firma
Copiamos el nuevo token generado a la cookie y recargamos la pagina
picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
## Notas

## Referencias
