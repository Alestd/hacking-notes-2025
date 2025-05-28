#### Description

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag

# Solución
 
````
└─$ wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
--2025-05-27 19:54:18--  https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 202940 (198K) [application/octet-stream]
Saving to: ‘mystery’

mystery                                   100%[====================================================================================>] 198.18K  1.16MB/s    in 0.2s    

2025-05-27 19:54:19 (1.16 MB/s) - ‘mystery’ saved [202940/202940]

                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ file mystery
mystery: data
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ xxd mystery | head
00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ cat mystery
�eN4
C"DRj|��xsRGB���gAMA��
pt��Ak�����>}*"3o�[U�==� ��8q"2�OW��%���[,��b�X,��b�X,��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g��b�X,��b�X,�E����b�X,��b�X,��b�e}}�X,��b�X,��b�XtY_�-��b�X,��b�X,]��g�o�����i�`�X,��b�X,��b�����;�������b�X,��b�X,��!�������▒�7eZIĶX,��b�X,��b1f}}���ѷ`�u▒���ڼ��b�X,_
                                             ����
└─$ 1;2c1;2c
1: command not found
2c1: command not found
2c: command not found
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ hexeditor mystery

zsh: suspended  hexeditor mystery
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ sudo apt install pngcheck
[sudo] password for kali: 
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Installing:
  pngcheck
                                                                                                                                                                       
Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 1477
  Download size: 68.6 kB
  Space needed: 208 kB / 58.9 GB available

Get:1 http://kali.download/kali kali-rolling/main amd64 pngcheck amd64 3.0.3-3 [68.6 kB]
Fetched 68.6 kB in 1s (134 kB/s)  
Selecting previously unselected package pngcheck.
(Reading database ... 405752 files and directories currently installed.)
Preparing to unpack .../pngcheck_3.0.3-3_amd64.deb ...
Unpacking pngcheck (3.0.3-3) ...
Setting up pngcheck (3.0.3-3) ...
Processing triggers for man-db (2.13.0-1) ...
Processing triggers for kali-menu (2024.4.0) ...
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ pngcheck -v mystery

picoCTF{c0rrupt10n_1847995}


```