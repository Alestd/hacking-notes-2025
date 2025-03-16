#### Description

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)

#### Hints 

To view the file in the webshell, do: `$ nano fixme2.py`

# Solución


```
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/5/fixme2.py
--2025-03-13 02:09:37--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py              100%[============================>]   1.00K  --.-KB/s    in 0s      

2025-03-13 02:09:37 (733 MB/s) - 'fixme2.py' saved [1029/1029]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        README.txt         codebook.txt  files      fixme2.py  strings
Addadshashanammu.zip    big-zip-files.zip  convertme.py  files.zip  runme.py
Addadshashanammu.zip.1  code.py            enc_flag      fixme1.py  static
alestd-picoctf@webshell:~$ python fixme2.py
  File "/home/alestd-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
alestd-picoctf@webshell:~$ nano fixme2.py
alestd-picoctf@webshell:~$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
alestd-picoctf@webshell:~$ 

```