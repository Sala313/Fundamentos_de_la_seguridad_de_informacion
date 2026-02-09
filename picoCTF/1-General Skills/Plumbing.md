## Descripcion
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?Connect to fickle-tempest.picoctf.net 54968.
## Solucion
```
nc fickle-tempest.picoctf.net 50730 > salida
^C
cat salida | grep pico
picoCTF{digital_plumb3r_0BAc587E}
```
## Notas
Para referenciarlo a un archivo de texto ' > '
Para filtrar lo que hay en el archivo ' | '
## Referencias
