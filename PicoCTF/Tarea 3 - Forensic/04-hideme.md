#### Description

Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/258/flag.png).

# Solución 

````
└─$ wget https://artifacts.picoctf.net/c/258/flag.png                        
--2025-05-28 18:54:31--  https://artifacts.picoctf.net/c/258/flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 42937 (42K) [application/octet-stream]
Saving to: ‘flag.png’

flag.png                                  100%[===================================================================================>]  41.93K  --.-KB/s    in 0.05s   

2025-05-28 18:54:31 (870 KB/s) - ‘flag.png’ saved [42937/42937]

                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ zsteg flag.png
zsteg: command not found
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ sudo apt install foremost
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Installing:
  foremost

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 1474
  Download size: 42.5 kB
  Space needed: 104 kB / 58.4 GB available

Get:1 http://http.kali.org/kali kali-rolling/main amd64 foremost amd64 1.5.7-11+b2 [42.5 kB]
Fetched 42.5 kB in 1s (57.0 kB/s)   
Selecting previously unselected package foremost.
(Reading database ... 405872 files and directories currently installed.)
Preparing to unpack .../foremost_1.5.7-11+b2_amd64.deb ...
Unpacking foremost (1.5.7-11+b2) ...
Setting up foremost (1.5.7-11+b2) ...
Processing triggers for man-db (2.13.0-1) ...
Processing triggers for kali-menu (2024.4.0) ...
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ sudo apt-get install zsteg

Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package zsteg
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ zsteg flag.png            
zsteg: command not found
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ foremost flag.png
Processing: flag.png
|foundat=secret/UT
foundat=secret/flag.pngUT
*|
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cd output
                                                                                                                                                                      
┌──(kali㉿kali)-[~/output]
└─$ cd zip
                                                                                                                                                                      
┌──(kali㉿kali)-[~/output/zip]
└─$ 7z x 00000077.zip

7-Zip 24.08 (x64) : Copyright (c) 1999-2024 Igor Pavlov : 2024-08-11
 64-bit locale=en_US.UTF-8 Threads:2 OPEN_MAX:1024

Scanning the drive for archives:
1 file, 3198 bytes (4 KiB)

Extracting archive: 00000077.zip
--
Path = 00000077.zip
Type = zip
Physical Size = 3198

Everything is Ok

Folders: 1
Files: 1
Size:       3029
Compressed: 3198
                                                                                                                                                                      
┌──(kali㉿kali)-[~/output/zip]
└─$ cd secret
                                                                                                                                                                      
┌──(kali㉿kali)-[~/output/zip/secret]
└─$ xdg-open flag.png


picoCTF{Hiddinng_An_imag3_within_@n_ima9e_d55982e8}
```