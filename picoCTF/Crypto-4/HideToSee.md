## Descripcion
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/241/atbash.jpg).
## Solucion
picoCTF{atbash_crack_7142fde9}
## Notas
```
steghide extract -sf atbash.jpg
 
cat encrypted.txt
```
[Atbash Cipher - Reverse Mirror Alphabet - Online Decoder/Translator](https://www.dcode.fr/atbash-cipher)
## Referencias

[picoCTF-2023-writeup/Cryptography/HideToSee/HideToSee.md at main · DanArmor/picoCTF-2023-writeup · GitHub](https://github.com/DanArmor/picoCTF-2023-writeup/blob/main/Cryptography/HideToSee/HideToSee.md)