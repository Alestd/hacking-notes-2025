

```
alestd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
--2025-02-17 18:21:00--  https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                   100%[============================>]  10.68K  --.-KB/s    in 0s      

2025-02-17 18:21:00 (324 MB/s) - 'warm' saved [10936/10936]

alestd-picoctf@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=506b7be935d8940c672ab0d40d2e03ebd746155b, with debug_info, not stripped
alestd-picoctf@webshell:~$ chmod +x warm
alestd-picoctf@webshell:~$ ls
README.txt  file  flag  nano.256.save  salida  warm
alestd-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
alestd-picoctf@webshell:~$ -h
-bash: -h: command not found
alestd-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
```