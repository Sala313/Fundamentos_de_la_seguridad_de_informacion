## Descripcion
Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:51158/
## Solucion
```
or i in {1..20}; do curl -s http://wily-courier.picoctf.net:51158/check -H "Cookie: name=$i" | grep pico
<p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
```
## Notas

## Referencias
