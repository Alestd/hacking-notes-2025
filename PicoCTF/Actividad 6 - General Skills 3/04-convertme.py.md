#### Description

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/22/convertme.py)

```
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/22/convertme.py
--2025-03-13 01:38:10--  https://artifacts.picoctf.net/c/22/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py           100%[============================>]   1.16K  --.-KB/s    in 0s      

2025-03-13 01:38:10 (493 MB/s) - 'convertme.py' saved [1189/1189]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        README.txt         codebook.txt  files      static
Addadshashanammu.zip    big-zip-files.zip  convertme.py  files.zip  strings
Addadshashanammu.zip.1  code.py            enc_flag      runme.py
alestd-picoctf@webshell:~$ python convertme.py
If 94 is in decimal base, what is it in binary base?
Answer: 1011110
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_762f748e}
```