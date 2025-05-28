#### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/212/disk.flag.img.gz)
  
  
  # Solución 
  
````
└─$ wget https://artifacts.picoctf.net/c/212/disk.flag.img.gz
--2025-05-28 12:35:03--  https://artifacts.picoctf.net/c/212/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.61, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 44360923 (42M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz                          100%[===================================================================================>]  42.31M  12.3MB/s    in 3.5s    

2025-05-28 12:35:07 (12.1 MB/s) - ‘disk.flag.img.gz’ saved [44360923/44360923]

                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ gunzip disk.flag.img.gz
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ fls -o 411648 disk.flag.img
d/d 460:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 81: proc
d/d 82: dev
d/d 83: tmp
d/d 84: lib
d/d 87: var
d/d 96: usr
d/d 106:        bin
d/d 120:        sbin
d/d 466:        media
d/d 470:        mnt
d/d 471:        opt
d/d 472:        root
d/d 473:        run
d/d 475:        srv
d/d 476:        sys
d/d 2041:       swap
V/V 51001:      $OrphanFiles
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ fls -o 411648 disk.flag.img 472
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ strings -t d disk.flag.img | grep -iE "flag.txt"
218985524 flag.txt
218985540 flag.txt.enc
219964416 touch flag.txt
219964431 nano flag.txt 
219964483 nano flag.txt 
219964506 openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
219964588 shred -u flag.txt
303193140 flag.txt
303317044 flag.txt
303317060 flag.txt.enc
303328308 flag.txt
303328324 flag.txt.enc
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ icat disk.flag.img -o 411648 1782 > flag.txt.enc
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ openssl aes256 -d -salt --in flag.txt.enc -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
4007BF7C697F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
picoCTF{h4un71ng_p457_0a710765} 

```