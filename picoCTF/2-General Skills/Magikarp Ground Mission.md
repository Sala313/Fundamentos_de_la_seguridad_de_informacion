## Descripcion
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `61637`.
## Solucion
```
ssh -p 54840 ctf-player@wily-courier.picoctf.net
ls
	1of3.flag.txt  instructions-to-2of3.txt
cat 1of3.flag.txt
	picoCTF{xxsh_
cat instructions-to-2of3.txt
	Next, go to the root of all things, more succinctly `/`
cd /
ls
	2of3.flag.txt  boot       dev  home                      lib    media  opt   root  sbin  sys  usr
	bin            challenge  etc  instructions-to-3of3.txt  lib64  mnt    proc  run   srv   tmp  var
cat 2of3.flag.txt
	0ut_0f_//4t3r_
cat instructions-to-3of3.txt
	Lastly, ctf-player, go home... more succinctly `~`
cd ~
ls
	3of3.flag.txt  drop-in
cat 3of3.flag.txt
	0b24fc4f}


```
## Notas
cd / se dirige a la raiz
cd ~ se dirige a home
cd .. sube un nivel hacia atras en las carpetas
## Referencias
