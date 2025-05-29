#### Description

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf).


# Solución

````
└─$ wget https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf
--2025-05-28 19:10:06--  https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf                        100%[===================================================================================>]   3.28K  --.-KB/s    in 0s      

2025-05-28 19:10:07 (114 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]

                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ file flag2of2-final.pdf
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ xdg-open flag2of2-final.pdf
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ mv flag2of2-final.pdf flag2of2-final.png

┌──(kali㉿kali)-[~]
└─$ xdg-open flag2of2-final.png

picoCTF{f1u3n7_1n_pn9_&_pdf_1f991f77}


```