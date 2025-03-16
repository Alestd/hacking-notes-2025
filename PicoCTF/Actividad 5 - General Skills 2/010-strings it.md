#### Description

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?


#### Hints 

[strings](https://linux.die.net/man/1/strings)

```
alestd-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
--2025-03-12 22:58:21--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                100%[============================>] 757.84K  1.86MB/s    in 0.4s    

2025-03-12 22:58:21 (1.86 MB/s) - 'strings' saved [776032/776032]

alestd-picoctf@webshell:~$ ls
Addadshashanammu      Addadshashanammu.zip.1  big-zip-files.zip  files      static
Addadshashanammu.zip  README.txt              enc_flag           files.zip  strings
alestd-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}


```

