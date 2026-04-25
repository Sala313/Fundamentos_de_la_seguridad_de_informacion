## Descripcion
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/127/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solucion
picoCTF{R0UND_N_R0UND_79C18FB3}
## Notas
```
cat message.txt | sed -e "s/^/[/" | sed 's/ *$//' | sed -e "s/$/]/" | sed -e "s/ /, /g"

arr = [128, 322, 353, 235, 336, 73, 198, 332, 202, 285, 57, 87, 262, 221, 218, 405, 335, 101, 256, 227, 112, 140]
characterSet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
flag = "picoCTF{"

for i in range(len(arr)):
	arr[i] = arr[i] % 37
	flag += characterSet[arr[i]]

flag += "}"
print(flag)
```
## Referencias

[picoCTF-2022-Writeup/Cryptography/basic-mod1/basic-mod1.md at main · noamgariani11/picoCTF-2022-Writeup · GitHub](https://github.com/noamgariani11/picoCTF-2022-Writeup/blob/main/Cryptography/basic-mod1/basic-mod1.md)