## Descripcion
This service provides you an encrypted flag. Can you decrypt it with just N & e?Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 50057`The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/c798cbe85b3e431345406f393827b9b905481b5fcd6d4b4a845527ee0602da9b/encrypt.py).
## Solucion
```
picoCTF{tw0_1$_pr!m341c6ed35}
```
## Notas
```
from Crypto.Util.number import long_to_bytes

N =19861705700941974807248932259594077238800008504038256014635143758710779941151531055283935868733930241550905175387297664679607989790375854942319441235413698
e = 65537

q = N // 2
phi_N = q - 1
d = pow(e, -1, phi_N)

c =  15200256002413673578151741206551467560507846666172634440888183559910928335420999496040005967329113336088009132420019188142835315084818803521799069036733771
m = pow(c, d, N)
flag = long_to_bytes(m)
print(flag)
```
## Referencias
[Even RSA Can Be Broken??? — picoCTF 2025 Challenge Write-Up | by Musthofa Kamaluddin | Medium](https://musthofa-kamaluddin.medium.com/even-rsa-can-be-broken-picoctf-2025-challenge-write-up-891447150064)
