## Descripcion
A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?Access the server using `nc verbal-sleep.picoctf.net 56684`
## Solucion
picoCTF{UseStr0nG_h@shEs_&PaSswDs!_5b836723}
## Notas
```                                                        
┌──(kali㉿kali)-[~/pico/crypto/hashcrack]
└─$ echo "482c811da5d5b4bc6d497ffa98491e38" > mis_hashes.txt
┌──(kali㉿kali)-[~/pico/crypto/hashcrack]
└─$ john --wordlist=rockyou.txt --format=Raw-MD5 mis_hashes.txt
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-MD5 [MD5 128/128 SSE2 4x3])
Warning: no OpenMP support for this hash type, consider --fork=4
Press 'q' or Ctrl-C to abort, almost any other key for status
password123      (?)     
1g 0:00:00:00 DONE (2026-04-26 11:42) 14.28g/s 21942p/s 21942c/s 21942C/s teacher..mexico1
Use the "--show --format=Raw-MD5" options to display all of the cracked passwords reliably
Session completed
┌──(kali㉿kali)-[~/pico/crypto/hashcrack]
└─$ echo "b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3" > mis_hashes.txt 
┌──(kali㉿kali)-[~/pico/crypto/hashcrack]
└─$ john --wordlist=rockyou.txt mis_hashes.txt                 
Warning: detected hash type "Raw-SHA1", but the string is also recognized as "Raw-SHA1-AxCrypt"
Use the "--format=Raw-SHA1-AxCrypt" option to force loading these as that type instead
Warning: detected hash type "Raw-SHA1", but the string is also recognized as "Raw-SHA1-Linkedin"
Use the "--format=Raw-SHA1-Linkedin" option to force loading these as that type instead
Warning: detected hash type "Raw-SHA1", but the string is also recognized as "ripemd-160"
Use the "--format=ripemd-160" option to force loading these as that type instead
Warning: detected hash type "Raw-SHA1", but the string is also recognized as "has-160"
Use the "--format=has-160" option to force loading these as that type instead
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-SHA1 [SHA1 128/128 SSE2 4x])
Warning: no OpenMP support for this hash type, consider --fork=4
Press 'q' or Ctrl-C to abort, almost any other key for status
letmein          (?)     
1g 0:00:00:00 DONE (2026-04-26 11:46) 25.00g/s 12800p/s 12800c/s 12800C/s fuckyou1..letmein
Use the "--show --format=Raw-SHA1" options to display all of the cracked passwords reliably
Session completed. 
┌──(kali㉿kali)-[~/pico/crypto/hashcrack]
└─$ echo "916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745" > mis_hashes.txt
┌──(kali㉿kali)-[~/pico/crypto/hashcrack]
└─$ john --wordlist=rockyou.txt --format=Raw-SHA256 mis_hashes.txt
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-SHA256 [SHA256 128/128 SSE2 4x])
Warning: poor OpenMP scalability for this hash type, consider --fork=4
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
qwerty098        (?)     
1g 0:00:00:00 DONE (2026-04-26 11:48) 11.11g/s 6917Kp/s 6917Kc/s 6917KC/s sammy82..magkawas
Use the "--show --format=Raw-SHA256" options to display all of the cracked passwords reliably
Session completed.
```
## Referencias

[PicoCTF Challenges: Hashcrack. Hello Cyber Enthusiasts, welcome to… | by Sparsh Ladani | InfoSec Write-ups](https://infosecwriteups.com/picoctf-challenges-hashcrack-09fddae4bb9b)