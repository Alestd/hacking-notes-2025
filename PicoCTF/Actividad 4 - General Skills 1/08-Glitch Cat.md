#### Description

Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.

#### Hints 

ASCII is one of the most common encodings used in programming
We know that the glitch output is valid Python, somehow!
Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Solución

```
alestd-picoctf@webshell:~$ nc saturn.picoctf.net 55575
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
alestd-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
'picoCTF{gl17ch_m3_n07_bda68f75}'
>>> 

'''
