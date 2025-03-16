#### Description

Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)   

#### Hints 

Try running the script and see what happens

# Solución 

```
alestd-picoctf@webshell:~$ wget 
wget: missing URL
Usage: wget [OPTION]... [URL]...

Try `wget --help' for more options.
alestd-picoctf@webshell:~$ alestd-picoctf@webshell:~$ python level3.py
-bash: alestd-picoctf@webshell:~$: command not found
alestd-picoctf@webshell:~$ Please enter correct password for flag: 87ab
-bash: Please: command not found
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/37/serpentine.py
--2025-03-13 03:21:18--  https://artifacts.picoctf.net/c/37/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py'

serpentine.py          100%[===========================>]   2.49K  --.-KB/s    in 0s      

2025-03-13 03:21:19 (1.11 GB/s) - 'serpentine.py' saved [2550/2550]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        codebook.txt  level1.flag.txt.enc  runme.py
Addadshashanammu.zip    convertme.py  level1.py            serpentine.py
Addadshashanammu.zip.1  enc_flag      level2.flag.txt.enc  static
README.txt              files         level2.py            strings
]                       files.zip     level3.flag.txt.enc
big-zip-files.zip       fixme1.py     level3.hash.bin
code.py                 fixme2.py     level3.py
alestd-picoctf@webshell:~$ python serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
You can do it!
-----------------------------------------------------


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
alestd-picoctf@webshell:~$ nano serpentine.py
alestd-picoctf@webshell:~$ python 
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5c) + chr(0x01) + chr(0x57) + chr(0x2a) + chr(0x17) + chr(0x5e) + chr(0x5f)
"\x15\x07\x08\x06'!#\x15\\\x01W*\x17^_"
alestd-picoctf@webshell:~$ python serpentine.py
  File "/home/alestd-picoctf/serpentine.py", line 80
    print_flag()
    ^
IndentationError: expected an indented block after 'if' statement on line 79
alestd-picoctf@webshell:~$ nano serpentine.py
alestd-picoctf@webshell:~$ python serpentine.py
picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}

```