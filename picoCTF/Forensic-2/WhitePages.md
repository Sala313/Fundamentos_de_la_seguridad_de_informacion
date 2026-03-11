## Descripcion
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/4de4b105d28cb6df34d9805217f2460b978a37dafc3dfc50edadd8d424dd311a/whitepages.txt) is all blank!
## Solucion
picoCTF{not_all_spaces_are_created_equal_f5d46aff52c6e17f9fd6317b33d2d783}
## Notas
```
from pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())

data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)

```
## Referencias
