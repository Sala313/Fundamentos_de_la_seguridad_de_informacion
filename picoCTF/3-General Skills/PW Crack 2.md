## Descripcion
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## Solucion
```
 nano level2.py y se modifica para que de la contrasena
 user_pw = input("Please enter correct password for flag: " + chr(0x33) >
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):

python3 level2.py
Please enter correct password for flag: 39ce39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```
## Notas

## Referencias