#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

#### Hints 

To view the file in the webshell, do: `$ nano level1.py`

# Solución 

````
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py
--2025-03-13 02:23:21--  https://artifacts.picoctf.net/c/11/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py              100%[============================>]     876  --.-KB/s    in 0s      

2025-03-13 02:23:21 (43.8 MB/s) - 'level1.py' saved [876/876]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        README.txt         codebook.txt  files      fixme2.py  static
Addadshashanammu.zip    big-zip-files.zip  convertme.py  files.zip  level1.py  strings
Addadshashanammu.zip.1  code.py            enc_flag      fixme1.py  runme.py
alestd-picoctf@webshell:~$ nano level1.py
alestd-picoctf@webshell:~$ python level1.py
Traceback (most recent call last):
  File "/home/alestd-picoctf/level1.py", line 13, in <module>
    flag_enc = open('level1.flag.txt.enc', 'rb').read()
FileNotFoundError: [Errno 2] No such file or directory: 'level1.flag.txt.enc'
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
--2025-03-13 02:24:54--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc    100%[============================>]      30  --.-KB/s    in 0s      

2025-03-13 02:24:54 (12.5 MB/s) - 'level1.flag.txt.enc' saved [30/30]

alestd-picoctf@webshell:~$ python level1.flag.txt.enc
  File "/home/alestd-picoctf/level1.flag.txt.enc", line 1
    A
     Rr1wQ      n
      ^
SyntaxError: invalid syntax
alestd-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 17ac
That password is incorrect
alestd-picoctf@webshell:~$ nano level1.py
alestd-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}



```