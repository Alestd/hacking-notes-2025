#### Description

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!

# Solución 

````
└─$ wget https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt
--2025-05-27 19:47:26--  https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2976 (2.9K) [application/octet-stream]
Saving to: ‘whitepages.txt’

whitepages.txt                            100%[====================================================================================>]   2.91K  --.-KB/s    in 0s      

2025-05-27 19:47:27 (34.4 MB/s) - ‘whitepages.txt’ saved [2976/2976]

                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ cat whitepages.txt
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ file whitepages.txt
whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators
whitepages.txt:: command not found
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ xxd whitepages.txt | head
00000000: e280 83e2 8083 e280 83e2 8083 20e2 8083  ............ ...
00000010: 20e2 8083 e280 83e2 8083 e280 83e2 8083   ...............
00000020: 20e2 8083 e280 8320 e280 83e2 8083 e280   ...... ........
00000030: 83e2 8083 20e2 8083 e280 8320 e280 8320  .... ...... ... 
00000040: 2020 e280 83e2 8083 e280 83e2 8083 e280    ..............
00000050: 8320 20e2 8083 20e2 8083 e280 8320 e280  .  ... ...... ..
00000060: 8320 20e2 8083 e280 83e2 8083 2020 e280  .  .........  ..
00000070: 8320 20e2 8083 2020 2020 e280 8320 e280  .  ...    ... ..
00000080: 83e2 8083 e280 83e2 8083 2020 e280 8320  ..........  ... 
00000090: e280 8320 e280 8320 e280 83e2 8083 e280  ... ... ........
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ python3 -m pip install pwntools 
Collecting pwntools
  Downloading pwntools-4.14.1-py2.py3-none-any.whl.metadata (5.3 kB)
Collecting paramiko>=1.15.2 (from pwntools)
  Downloading paramiko-3.5.1-py3-none-any.whl.metadata (4.6 kB)
Collecting mako>=1.0.0 (from pwntools)
  Downloading mako-1.3.10-py3-none-any.whl.metadata (2.9 kB)
Collecting pyelftools>=0.29 (from pwntools)
  Downloading pyelftools-0.32-py3-none-any.whl.metadata (372 bytes)
Collecting capstone>=3.0.5rc2 (from pwntools)
  Downloading capstone-6.0.0a4-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (3.8 kB)
Collecting ropgadget>=5.3 (from pwntools)
  Downloading ROPGadget-7.6-py3-none-any.whl.metadata (1.0 kB)
Collecting pyserial>=2.7 (from pwntools)
  Downloading pyserial-3.5-py2.py3-none-any.whl.metadata (1.6 kB)
Collecting requests>=2.0 (from pwntools)
  Using cached requests-2.32.3-py3-none-any.whl.metadata (4.6 kB)
Requirement already satisfied: pip>=6.0.8 in ./venv/lib/python3.13/site-packages (from pwntools) (24.3.1)
Collecting pygments>=2.0 (from pwntools)
  Downloading pygments-2.19.1-py3-none-any.whl.metadata (2.5 kB)
Collecting pysocks (from pwntools)
  Downloading PySocks-1.7.1-py3-none-any.whl.metadata (13 kB)
Collecting python-dateutil (from pwntools)
  Downloading python_dateutil-2.9.0.post0-py2.py3-none-any.whl.metadata (8.4 kB)
Collecting packaging (from pwntools)
  Downloading packaging-25.0-py3-none-any.whl.metadata (3.3 kB)
Collecting psutil>=3.3.0 (from pwntools)
  Downloading psutil-7.0.0-cp36-abi3-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (22 kB)
Collecting intervaltree>=3.0 (from pwntools)
  Downloading intervaltree-3.1.0.tar.gz (32 kB)
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting sortedcontainers (from pwntools)
  Downloading sortedcontainers-2.4.0-py2.py3-none-any.whl.metadata (10 kB)
Collecting unicorn!=2.1.3,>=2.0.1 (from pwntools)
  Downloading unicorn-2.1.2-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.2 kB)
Collecting six>=1.12.0 (from pwntools)
  Downloading six-1.17.0-py2.py3-none-any.whl.metadata (1.7 kB)
Collecting rpyc (from pwntools)
  Downloading rpyc-6.0.2-py3-none-any.whl.metadata (3.5 kB)
Collecting colored_traceback (from pwntools)
  Downloading colored_traceback-0.4.2-py3-none-any.whl.metadata (4.6 kB)
Collecting unix-ar (from pwntools)
  Downloading unix_ar-0.2.1-py2.py3-none-any.whl.metadata (1.9 kB)
Collecting zstandard (from pwntools)
  Downloading zstandard-0.23.0-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (3.0 kB)
Requirement already satisfied: MarkupSafe>=0.9.2 in ./venv/lib/python3.13/site-packages (from mako>=1.0.0->pwntools) (3.0.2)
Collecting bcrypt>=3.2 (from paramiko>=1.15.2->pwntools)
  Downloading bcrypt-4.3.0-cp39-abi3-manylinux_2_34_x86_64.whl.metadata (10 kB)
Collecting cryptography>=3.3 (from paramiko>=1.15.2->pwntools)
  Downloading cryptography-45.0.3-cp311-abi3-manylinux_2_34_x86_64.whl.metadata (5.7 kB)
Collecting pynacl>=1.5 (from paramiko>=1.15.2->pwntools)
  Downloading PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux_2_24_x86_64.whl.metadata (8.6 kB)
Collecting charset-normalizer<4,>=2 (from requests>=2.0->pwntools)
  Using cached charset_normalizer-3.4.2-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (35 kB)
Collecting idna<4,>=2.5 (from requests>=2.0->pwntools)
  Using cached idna-3.10-py3-none-any.whl.metadata (10 kB)
Collecting urllib3<3,>=1.21.1 (from requests>=2.0->pwntools)
  Using cached urllib3-2.4.0-py3-none-any.whl.metadata (6.5 kB)
Collecting certifi>=2017.4.17 (from requests>=2.0->pwntools)
  Using cached certifi-2025.4.26-py3-none-any.whl.metadata (2.5 kB)
Collecting plumbum (from rpyc->pwntools)
  Downloading plumbum-1.9.0-py3-none-any.whl.metadata (10 kB)
Collecting cffi>=1.14 (from cryptography>=3.3->paramiko>=1.15.2->pwntools)
  Downloading cffi-1.17.1-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (1.5 kB)
Collecting pycparser (from cffi>=1.14->cryptography>=3.3->paramiko>=1.15.2->pwntools)
  Downloading pycparser-2.22-py3-none-any.whl.metadata (943 bytes)
Downloading pwntools-4.14.1-py2.py3-none-any.whl (12.9 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.9/12.9 MB 12.3 MB/s eta 0:00:00
Downloading capstone-6.0.0a4-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (2.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.3/2.3 MB 11.3 MB/s eta 0:00:00
Downloading mako-1.3.10-py3-none-any.whl (78 kB)
Downloading paramiko-3.5.1-py3-none-any.whl (227 kB)
Downloading psutil-7.0.0-cp36-abi3-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (277 kB)
Downloading pyelftools-0.32-py3-none-any.whl (188 kB)
Downloading pygments-2.19.1-py3-none-any.whl (1.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.2/1.2 MB 11.5 MB/s eta 0:00:00
Downloading pyserial-3.5-py2.py3-none-any.whl (90 kB)
Using cached requests-2.32.3-py3-none-any.whl (64 kB)
Downloading ROPGadget-7.6-py3-none-any.whl (32 kB)
Downloading six-1.17.0-py2.py3-none-any.whl (11 kB)
Downloading sortedcontainers-2.4.0-py2.py3-none-any.whl (29 kB)
Downloading unicorn-2.1.2-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (16.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 16.3/16.3 MB 11.9 MB/s eta 0:00:00
Downloading colored_traceback-0.4.2-py3-none-any.whl (5.5 kB)
Downloading packaging-25.0-py3-none-any.whl (66 kB)
Downloading PySocks-1.7.1-py3-none-any.whl (16 kB)
Downloading python_dateutil-2.9.0.post0-py2.py3-none-any.whl (229 kB)
Downloading rpyc-6.0.2-py3-none-any.whl (74 kB)
Downloading unix_ar-0.2.1-py2.py3-none-any.whl (6.5 kB)
Downloading zstandard-0.23.0-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (5.4 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.4/5.4 MB 10.2 MB/s eta 0:00:00
Downloading bcrypt-4.3.0-cp39-abi3-manylinux_2_34_x86_64.whl (284 kB)
Using cached certifi-2025.4.26-py3-none-any.whl (159 kB)
Using cached charset_normalizer-3.4.2-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (148 kB)
Downloading cryptography-45.0.3-cp311-abi3-manylinux_2_34_x86_64.whl (4.5 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 4.5/4.5 MB 11.6 MB/s eta 0:00:00
Using cached idna-3.10-py3-none-any.whl (70 kB)
Downloading PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux_2_24_x86_64.whl (856 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 856.7/856.7 kB 9.6 MB/s eta 0:00:00
Using cached urllib3-2.4.0-py3-none-any.whl (128 kB)
Downloading plumbum-1.9.0-py3-none-any.whl (127 kB)
Downloading cffi-1.17.1-cp313-cp313-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (479 kB)
Downloading pycparser-2.22-py3-none-any.whl (117 kB)
Building wheels for collected packages: intervaltree
  Building wheel for intervaltree (pyproject.toml) ... done
  Created wheel for intervaltree: filename=intervaltree-3.1.0-py2.py3-none-any.whl size=26190 sha256=7f03574133a953d20c0fe35bc69c1912faebeae82bd16eb26567130700ceb906
  Stored in directory: /home/kali/.cache/pip/wheels/a7/d2/99/50f53015b573c9b65ff643d7f213fc7784dad87976e79cf02c
Successfully built intervaltree
Installing collected packages: sortedcontainers, pyserial, pyelftools, zstandard, urllib3, unix-ar, unicorn, six, pysocks, pygments, pycparser, psutil, plumbum, packaging, mako, intervaltree, idna, charset-normalizer, certifi, capstone, bcrypt, rpyc, ropgadget, requests, python-dateutil, colored_traceback, cffi, pynacl, cryptography, paramiko, pwntools
Successfully installed bcrypt-4.3.0 capstone-6.0.0a4 certifi-2025.4.26 cffi-1.17.1 charset-normalizer-3.4.2 colored_traceback-0.4.2 cryptography-45.0.3 idna-3.10 intervaltree-3.1.0 mako-1.3.10 packaging-25.0 paramiko-3.5.1 plumbum-1.9.0 psutil-7.0.0 pwntools-4.14.1 pycparser-2.22 pyelftools-0.32 pygments-2.19.1 pynacl-1.5.0 pyserial-3.5 pysocks-1.7.1 python-dateutil-2.9.0.post0 requests-2.32.3 ropgadget-7.6 rpyc-6.0.2 six-1.17.0 sortedcontainers-2.4.0 unicorn-2.1.2 unix-ar-0.2.1 urllib3-2.4.0 zstandard-0.23.0
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ nano exp.py

b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}\n\t\t'

picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}

```