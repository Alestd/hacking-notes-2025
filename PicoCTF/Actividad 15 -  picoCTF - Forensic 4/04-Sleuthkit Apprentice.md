#### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)
  
# Solucion
   
````
└─$ wget https://artifacts.picoctf.net/c/136/disk.flag.img.gz
--2025-05-28 10:39:21--  https://artifacts.picoctf.net/c/136/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.61, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534571 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz                          100%[===================================================================================>]  45.33M  12.6MB/s    in 3.9s    

2025-05-28 10:39:25 (11.7 MB/s) - ‘disk.flag.img.gz’ saved [47534571/47534571]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ gunzip disk.flag.img.gz
                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ fls -o 360448 disk.flag.img 3981
r/r * 2082(realloc):    flag.txt
r/r 2371:       flag.uni.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ icat -o 360448 disk.flag.img 2371
picoCTF{by73_5urf3r_3497ae6b}



```