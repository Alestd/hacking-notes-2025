#### Description

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.

#### Hints 

1.- I hear python can convert things.
2.-It might help to have multiple windows open
# Solución 

[From Octal - CyberChef](https://cyberchef.org/#recipe=From_Octal\('Space'\)&input=MTU0IDE1MSAxNzIgMTQxIDE2MiAxNDQ)
[Hex to String | Hex to ASCII Converter](https://www.rapidtables.com/convert/number/hex-to-ascii.html)

```
alestd-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
lamp
Please give the 01101100 01100001 01101101 01110000 as a word.
...
you have 45 seconds.....

Input:
lamp
Please give me the  154 151 172 141 162 144 as a word.
Input:
lizard
Please give me the 636f6d7075746572 as a word.
Input:
computer
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}

```
