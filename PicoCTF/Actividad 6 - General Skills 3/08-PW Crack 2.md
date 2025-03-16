#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.

#### Hints 

Does that encoding look familiar?

# Solución 

```

alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.py
--2025-03-13 02:52:13--  https://artifacts.picoctf.net/c/14/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                       100%[=====================================================================================================>]     914  --.-KB/s    in 0s      

2025-03-13 02:52:13 (331 MB/s) - 'level2.py' saved [914/914]

alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
--2025-03-13 02:53:24--  https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                             100%[=====================================================================================================>]      31  --.-KB/s    in 0s      

2025-03-13 02:53:24 (9.36 MB/s) - 'level2.flag.txt.enc' saved [31/31]

alestd-picoctf@webshell:~$ ls
Addadshashanammu      Addadshashanammu.zip.1  big-zip-files.zip  codebook.txt  enc_flag  files.zip  fixme2.py            level1.py            level2.py  static
Addadshashanammu.zip  README.txt              code.py            convertme.py  files     fixme1.py  level1.flag.txt.enc  level2.flag.txt.enc  runme.py   strings
alestd-picoctf@webshell:~$ python level2.py
Please enter correct password for flag: er
That password is incorrect
alestd-picoctf@webshell:~$ nano level2.py
alestd-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)
'4ec9'
alestd-picoctf@webshell:~$ python level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}

```