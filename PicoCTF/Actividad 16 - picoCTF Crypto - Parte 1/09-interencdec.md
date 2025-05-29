#### Description

Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/2/enc_flag).

# Solución

````
└─$ wget https://artifacts.picoctf.net/c_titan/2/enc_flag                                        
--2025-05-28 22:33:10--  https://artifacts.picoctf.net/c_titan/2/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.64, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag                                  100%[====================================================================================>]      73  --.-KB/s    in 0s      

2025-05-28 22:33:10 (47.4 MB/s) - ‘enc_flag’ saved [73/73]

                                                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6YzRNalV3YUcxcWZRPT0nCg==
                                                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ echo YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6YzRNalV3YUcxcWZRPT0nCg== | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ=='
                                                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ echo d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ== | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_78250hmj}


Input: wpjvJAM{jhlzhy_k3jy9wa3k_78250hmj}
Recipe: ROT19
Flag: picoCTF{caesar_d3cr9pt3d_78250afc}

```