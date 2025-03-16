
#### Description

Can you convert the number 42 (base 10) to binary (base 2)?

### Hints
Submit your answer in our competition's flag format. For example, if your answer was '11111', you would submit 'picoCTF{11111}' as the flag.

### Solución 
 ````
alestd-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin (42)
'0b101010'
>>> bin (42)[:2]
'0b'
>>> bin (42)[2:]
'101010'
picoCTF{101010}
```
