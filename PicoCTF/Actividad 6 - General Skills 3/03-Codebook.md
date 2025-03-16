#### Description

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)
#### Hints 

1.-On the webshell, use `ls` to see if both files are in the directory you are in
2.-The `str_xor` function does not need to be reverse engineered for this challenge.

# solución

```
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/3/code.py
--2025-03-13 01:33:45--  https://artifacts.picoctf.net/c/3/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                100%[============================>]   1.25K  --.-KB/s    in 0s      

2025-03-13 01:33:45 (583 MB/s) - 'code.py' saved [1278/1278]

alestd-picoctf@webshell:~$ https://artifacts.picoctf.net/c/3/codebook.txt
-bash: https://artifacts.picoctf.net/c/3/codebook.txt: No such file or directory
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2025-03-13 01:34:12--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt           100%[============================>]      27  --.-KB/s    in 0s      

2025-03-13 01:34:12 (9.03 MB/s) - 'codebook.txt' saved [27/27]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        README.txt         codebook.txt  files.zip  strings
Addadshashanammu.zip    big-zip-files.zip  enc_flag      runme.py
Addadshashanammu.zip.1  code.py            files         static
alestd-picoctf@webshell:~$ python code.py
picoCTF{c0d3b00k_455157_197a982c}
```