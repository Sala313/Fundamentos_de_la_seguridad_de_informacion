## Descripcion
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/258/flag.png).
## Solucion
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_d55982e8}
## Notas
```
binwalk -e flag.png
cd _flag.png.extracted
ls -la
cd secret
open flag.png
```
## Referencias

