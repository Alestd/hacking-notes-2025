#### Description

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!

#### Hints 

(None)

## Solucion

```
alestd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
--2025-03-12 22:28:51--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                 100%[============================>]   8.18K  --.-KB/s    in 0s      

2025-03-12 22:28:51 (108 MB/s) - 'static' saved [8376/8376]

alestd-picoctf@webshell:~$ ls
Addadshashanammu      Addadshashanammu.zip.1  big-zip-files.zip  files      static
Addadshashanammu.zip  README.txt              enc_flag           files.zip
alestd-picoctf@webshell:~$ strings static | grep picoCTF                                   
picoCTF{d15a5m_t34s3r_f5aeda17}

```