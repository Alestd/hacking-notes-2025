#### Description

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/160/challenge.zip)
#### Hints 

1.-The `cat` command will let you read a file, but that won't help you here!
2.- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3.-When committing a file with git, a message can (and should) be included.
# Solución 

````
alestd-picoctf@webshell:~$ ls
challenge.zip  drop-in
alestd-picoctf@webshell:~$ cd drop-in/
alestd-picoctf@webshell:~/drop-in$ git log

[2]+  Stopped                 git log
commit 89d296ef533525a1378529be66b22d6a2c01e530 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:22 2024 +0000

    picoCTF{t1m3m@ch1n3_186cd7d7}
```