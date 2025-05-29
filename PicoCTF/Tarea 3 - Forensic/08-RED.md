#### Description

RED, RED, RED, REDDownload the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)

# Solución


````
└─$ wget https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png
--2025-05-28 19:16:13--  https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 65.9.149.59, 65.9.149.85, 65.9.149.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|65.9.149.59|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 796 [application/octet-stream]
Saving to: ‘red.png’

red.png                                   100%[===================================================================================>]     796  --.-KB/s    in 0s      

2025-05-28 19:16:13 (14.3 MB/s) - ‘red.png’ saved [796/796]

                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ file red.png
red.png: PNG image data, 128 x 128, 8-bit/color RGBA, non-interlaced
┌──(kali㉿kali)-[~]
└─$ echo cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ== |
base64 -d
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}  

```