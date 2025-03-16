#### Description

What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

### Hints
Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

### Solución 1 usando cyberchef
``
```
Input: bDNhcm5fdGgzX3IwcDM1
Output: l3arn_th3_r0p35
picoCTF{l3arn_th3_r0p35}
```
### Solucion 2 usando python

```
alestd-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1 | base64 -d
l3arn_th3_r0p35alestd-picoctf@webshell:~$ 
alestd-picoctf@webshell:~$ 

```