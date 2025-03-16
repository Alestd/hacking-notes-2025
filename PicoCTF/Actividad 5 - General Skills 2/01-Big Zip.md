### Description

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)


## Hints

Can grep be instructed to look at every file in a directory and its subdirectories? 

```
alestd-picoctf@webshell:~$ wget Big Zip                                     
--2025-02-17 19:18:36--  http://big/
Resolving big (big)... failed: Name or service not known.
wget: unable to resolve host address 'big'
--2025-02-17 19:18:36--  http://zip/
Resolving zip (zip)... failed: No address associated with hostname.
wget: unable to resolve host address 'zip'
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/504/big-zip-files.zip
--2025-02-17 19:19:07--  https://artifacts.picoctf.net/c/504/big-zip-files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3182988 (3.0M) [application/octet-stream]
Saving to: 'big-zip-files.zip'

big-zip-files.zip      100%[============================>]   3.04M  1.78MB/s    in 1.7s    

2025-02-17 19:19:08 (1.78 MB/s) - 'big-zip-files.zip' saved [3182988/3182988]

alestd-picoctf@webshell:~$ grep -R picoCTF
grep: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet: binary file matches
alestd-picoctf@webshell:~$ Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
*ZAP!* picoCTF{gr3p_15_m4g1c_ef8790dc}


```