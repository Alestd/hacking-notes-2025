#### Description

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz)

Hints: Have you ever used `file` to determine what a file was? Relevant terminal-fu in picoGym: [https://play.picoctf.org/practice/challenge/85](https://play.picoctf.org/practice/challenge/85) Mastering this terminal-fu would enable you to find the flag in a single command: [https://play.picoctf.org/practice/challenge/48](https://play.picoctf.org/practice/challenge/48) Using your own computer, you could use qemu to boot from this disk!
# Solución

````
└─$ wget https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz
--2025-05-28 10:32:50--  https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz                   100%[===================================================================================>]  28.39M  10.1MB/s    in 2.8s    

2025-05-28 10:32:54 (10.1 MB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ gunzip dds1-alpine.flag.img.gz
                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ sudo apt install autopsy
autopsy is already the newest version (2.24-6kali1).
autopsy set to manually installed.
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 1474
                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ srch_strings dds1-alpine.flag.img | grep picoCTF
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}


```