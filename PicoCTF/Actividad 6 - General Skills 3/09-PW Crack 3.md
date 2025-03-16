#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

#### Hints 

1.-To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`

2.-To exit `bvi` type `:q` and press enter.

# Solución

```
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2025-03-13 03:06:30--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc    100%[===========================>]      31  --.-KB/s    in 0s      

2025-03-13 03:06:30 (1.55 MB/s) - 'level3.flag.txt.enc' saved [31/31]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        code.py       fixme1.py            level3.flag.txt.enc
Addadshashanammu.zip    codebook.txt  fixme2.py            runme.py
Addadshashanammu.zip.1  convertme.py  level1.flag.txt.enc  static
README.txt              enc_flag      level1.py            strings
]                       files         level2.flag.txt.enc
big-zip-files.zip       files.zip     level2.py
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
--2025-03-13 03:06:59--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin        100%[===========================>]      16  --.-KB/s    in 0s      

2025-03-13 03:06:59 (1.04 MB/s) - 'level3.hash.bin' saved [16/16]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        code.py       fixme1.py            level3.flag.txt.enc
Addadshashanammu.zip    codebook.txt  fixme2.py            level3.hash.bin
Addadshashanammu.zip.1  convertme.py  level1.flag.txt.enc  runme.py
README.txt              enc_flag      level1.py            static
]                       files         level2.flag.txt.enc  strings
big-zip-files.zip       files.zip     level2.py
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py
--2025-03-13 03:07:48--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py              100%[===========================>]   1.31K  --.-KB/s    in 0s      

2025-03-13 03:07:48 (56.1 MB/s) - 'level3.py' saved [1337/1337]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        code.py       fixme1.py            level3.flag.txt.enc
Addadshashanammu.zip    codebook.txt  fixme2.py            level3.hash.bin
Addadshashanammu.zip.1  convertme.py  level1.flag.txt.enc  level3.py
README.txt              enc_flag      level1.py            runme.py
]                       files         level2.flag.txt.enc  static
big-zip-files.zip       files.zip     level2.py            strings
alestd-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: re
That password is incorrect
alestd-picoctf@webshell:~$ nano level3.py
alestd-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 3961
That password is incorrect
alestd-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 752e
That password is incorrect
alestd-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: f159
That password is incorrect
alestd-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: dba8
That password is incorrect
alestd-picoctf@webshell:~$ python level3.py
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}

```