## Descripcion
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/178/challenge.zip)
## Solucion
```
git branch -a
	feature/part-1
	feature/part-2
	feature/part-3
	* main
	master

cat flag.py
	print("Printing the flag...")

git checkout -f feature/part-1
	Switched to branch 'feature/part-1'
cat flag.py
	print("Printing the flag...")
	print("picoCTF{t3@mw0rk_", end='')
git checkout -f feature/part-2
	Switched to branch 'feature/part-2'
cat flag.py
	print("Printing the flag...")
	print("m@k3s_th3_dr3@m_", end='')
git checkout -f feature/part-3
	Switched to branch 'feature/part-3'
cat flag.py
	print("Printing the flag...")
	print("w0rk_6c06cec1}")
```
## Notas

## Referencias

