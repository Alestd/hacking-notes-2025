#### Description

Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)
#### Hints 
1.-In collaborative projects, many users can make many changes. How can you see the changes within one file?
2.-Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3.-You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.

# Solución

```
alestd-picoctf@webshell:~$ ls
README.txt  challenge.zip  drop-in
alestd-picoctf@webshell:~$ cd drop-in/
alestd-picoctf@webshell:~/drop-in$ ls
message.py
alestd-picoctf@webshell:~/drop-in$ ls -al
total 8
drwxr-xr-x 3 alestd-picoctf alestd-picoctf   36 Mar  9  2024 .
drwxr-xr-x 5 alestd-picoctf alestd-picoctf 4096 Mar 14 02:24 ..
drwxr-xr-x 8 alestd-picoctf alestd-picoctf  166 Mar  9  2024 .git
-rw-r--r-- 1 alestd-picoctf alestd-picoctf   22 Mar  9  2024 message.py
alestd-picoctf@webshell:~/drop-in$ cd .git
alestd-picoctf@webshell:~/drop-in$ git log

[1]+  Stopped                 git log
alestd-picoctf@webshell:~/drop-in$ git reflog

[2]+  Stopped                 git reflog
alestd-picoctf@webshell:~/drop-in$ git checkout faddeca9
error: pathspec 'faddeca9' did not match any file(s) known to git
alestd-picoctf@webshell:~/drop-in$ git checkout 2dd4676 
Note: switching to '2dd4676'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 2dd4676 create top secret project
alestd-picoctf@webshell:~/drop-in$ git checkout fadeca9
Previous HEAD position was 2dd4676 create top secret project
HEAD is now at fadeca9 optimize file size of prod code
alestd-picoctf@webshell:~/drop-in$ git log

[4]+  Stopped                 git log

commit fadeca9476b6713ec8cdda633aca9e9aebffc698 (HEAD)
Author: picoCTF{@sk_th3_1nt3rn_e9957ce1} <ops@picoctf.com>
Date:   Sat Mar 9 21:09:11 2024 +0000

    optimize file size of prod code

commit 2dd46769e2d65656bb14aed0ff5d3237daaa7d9d
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:11 2024 +0000

    create top secret project
picoCTF{@sk_th3_1nt3rn_e9957ce1}
```