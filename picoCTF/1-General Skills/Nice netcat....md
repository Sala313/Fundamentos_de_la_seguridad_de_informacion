## Descripcion
There is a nice program that you can talk to by using this command in a shell:$ nc wily-courier.picoctf.net 64321, but it doesn't speak English...
## Solucion
```
>>> list = [112,105,99,111,67,84,70,123,103,48,48,100,95,107,49,116,116,121,33,95,110,49,99,51,95,107,49,116,116,121,33,95,49,57,53,102,101,125,10]
>>>  for i in list:
...  print(chr(i))

```
picoCTF{g00d_k1tty!_n1c3_k1tty!_195fe}
## Notas

## Referencias


