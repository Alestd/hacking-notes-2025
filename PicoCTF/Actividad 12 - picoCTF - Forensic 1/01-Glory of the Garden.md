#### Description

This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems

# Solución

````
└─$ wget https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg
--2025-05-27 19:25:01--  https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg                                100%[====================================================================================>]   2.19M  3.48MB/s    in 0.6s    

2025-05-27 19:25:02 (3.48 MB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ hexeditor garden.jpg
                                                                                                                                                                       

┌──(venv)─(kali㉿kali)-[~]
└─$ strings garden.jpg | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y3eBdBd2cc}"


picoCTF{more_than_m33ts_the_3y3eBdBd2cc}

```