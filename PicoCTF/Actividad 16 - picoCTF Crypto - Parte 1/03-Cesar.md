#### Description

Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext).

# Solución

````
└─$ wget https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
--2025-05-28 21:12:01--  https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext                                100%[===================================================================================>]      35  --.-KB/s    in 0s      

2025-05-28 21:12:02 (27.1 MB/s) - ‘ciphertext’ saved [35/35]

                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cat ciphertext
picoCTF{ynkooejcpdanqxeykjrbdofgkq} 


picoCTF{crossingtherubiconvfhsjkou}

```