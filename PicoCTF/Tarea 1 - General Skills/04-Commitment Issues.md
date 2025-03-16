#### Description

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/138/challenge.zip)
#### Hints 

1.-You can 'checkout' commits to see the files inside them
2.-Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
3.-You can 'checkout' commits to see the files inside them
# Solucón

```

alestd-picoctf@webshell:~$ https://artifacts.picoctf.net/c_titan/138/challenge.zip
-bash: https://artifacts.picoctf.net/c_titan/138/challenge.zip: No such file or directory
alestd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/138/challenge.zip
--2025-03-14 01:53:51--  https://artifacts.picoctf.net/c_titan/138/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19199 (19K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip          100%[============================>]  18.75K  --.-KB/s    in 0.005s  

2025-03-14 01:53:51 (3.48 MB/s) - 'challenge.zip' saved [19199/19199]

alestd-picoctf@webshell:~$ ls
Addadshashanammu        challenge.zip  files.zip            level2.py            static
Addadshashanammu.zip    code.py        fixme1.py            level3.flag.txt.enc  strings
Addadshashanammu.zip.1  codebook.txt   fixme2.py            level3.hash.bin
README.txt              convertme.py   level1.flag.txt.enc  level3.py
]                       enc_flag       level1.py            runme.py
big-zip-files.zip       files          level2.flag.txt.enc  serpentine.py
alestd-picoctf@webshell:~$ unzip challenge.zip
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/0e/
 extracting: drop-in/.git/objects/0e/0fefcdc9c9722914a7a9ecab1e88784f005eeb  
   creating: drop-in/.git/objects/5b/
 extracting: drop-in/.git/objects/5b/222fb49097fe9874695e8cc7cd9a6c80886017  
   creating: drop-in/.git/objects/b5/
 extracting: drop-in/.git/objects/b5/62f0b425907789d11d2fe2793e67592dc6be93  
   creating: drop-in/.git/objects/d5/
 extracting: drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
   creating: drop-in/.git/objects/42/
 extracting: drop-in/.git/objects/42/942c9c605b30100f5d859ef6e172027447c0db  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
 extracting: drop-in/message.txt     
alestd-picoctf@webshell:~$ ls
Addadshashanammu        code.py       fixme1.py            level3.hash.bin
Addadshashanammu.zip    codebook.txt  fixme2.py            level3.py
Addadshashanammu.zip.1  convertme.py  level1.flag.txt.enc  runme.py
README.txt              drop-in       level1.py            serpentine.py
]                       enc_flag      level2.flag.txt.enc  static
big-zip-files.zip       files         level2.py            strings
challenge.zip           files.zip     level3.flag.txt.enc
alestd-picoctf@webshell:~$ ls -al
total 7924
drwxr-xr-x 7 alestd-picoctf alestd-picoctf    4096 Mar 14 01:54 .
drwxr-xr-x 3 root           root                28 Feb 10 18:16 ..
-rw------- 1 alestd-picoctf alestd-picoctf    2893 Mar 13 03:48 .bash_history
-rw-r--r-- 1 alestd-picoctf alestd-picoctf     220 Feb 10 18:16 .bash_logout
-rw-r--r-- 1 alestd-picoctf alestd-picoctf    3771 Feb 10 18:16 .bashrc
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    1024 Mar 13 01:19 .flag.swp
-rw------- 1 alestd-picoctf alestd-picoctf      20 Feb 12 18:48 .lesshst
drwxrwxr-x 3 alestd-picoctf alestd-picoctf      19 Feb 12 18:38 .local
-rw-r--r-- 1 alestd-picoctf alestd-picoctf     807 Feb 10 18:16 .profile
drwx------ 2 alestd-picoctf alestd-picoctf      48 Mar 14 01:33 .ssh
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf     167 Mar 12 22:58 .wget-hsts
drwxr-xr-x 3 alestd-picoctf alestd-picoctf      28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    4520 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    4520 Mar 16  2021 Addadshashanammu.zip.1
-rw-r--r-- 1 root           root              4443 Mar 14 01:19 README.txt
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf       0 Mar 13 02:58 ]
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf 3182988 Aug  4  2023 big-zip-files.zip
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf   19199 Mar 12  2024 challenge.zip
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    1278 Mar 16  2023 code.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf      27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    1189 Mar 16  2023 convertme.py
drwxr-xr-x 3 alestd-picoctf alestd-picoctf      49 Mar 12  2024 drop-in
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf     349 Mar 16  2023 enc_flag
drwxrwxr-x 5 alestd-picoctf alestd-picoctf     124 May 13  2022 files
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf 3995553 Aug  4  2023 files.zip
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf     868 Mar 13 02:03 fixme1.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    1030 Mar 13 02:16 fixme2.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf      30 Mar 16  2023 level1.flag.txt.enc
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf     876 Mar 16  2023 level1.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf      31 Mar 16  2023 level2.flag.txt.enc
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf     914 Mar 16  2023 level2.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf      31 Mar 16  2023 level3.flag.txt.enc
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf      16 Mar 16  2023 level3.hash.bin
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    1337 Mar 16  2023 level3.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf     270 Mar 16  2023 runme.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    2565 Mar 13 03:38 serpentine.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf    8376 Mar 16  2021 static
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf  776032 Oct 26  2020 strings
alestd-picoctf@webshell:~$ cd /
alestd-picoctf@webshell:/$ ls
bin   dev  home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  etc  lib   lib64  media   opt  root  sbin  sys  usr  wine
alestd-picoctf@webshell:/$ ls -al
total 4
drwxr-xr-x   1 root           root             55 Mar 14 01:19 .
drwxr-xr-x   1 root           root             55 Mar 14 01:19 ..
-rwxr-xr-x   1 root           root              0 Mar 14 01:19 .dockerenv
lrwxrwxrwx   1 root           root              7 Jan 26 02:05 bin -> usr/bin
drwxr-xr-x   2 root           root              6 Apr 18  2022 boot
drwxr-xr-x   5 root           root            360 Mar 14 01:19 dev
drwxr-xr-x   1 root           root           4096 Mar 14 01:19 etc
drwxr-xr-x   3 root           root             28 Feb 10 18:16 home
lrwxrwxrwx   1 root           root              7 Jan 26 02:05 lib -> usr/lib
lrwxrwxrwx   1 root           root              9 Jan 26 02:05 lib32 -> usr/lib32
lrwxrwxrwx   1 root           root              9 Jan 26 02:05 lib64 -> usr/lib64
lrwxrwxrwx   1 root           root             10 Jan 26 02:05 libx32 -> usr/libx32
drwxr-xr-x   2 root           root              6 Jan 26 02:05 media
drwxr-xr-x   2 root           root              6 Jan 26 02:05 mnt
drwxr-xr-x   1 root           root             24 Mar  5 02:10 opt
dr-xr-xr-x 822 root           root              0 Mar 14 01:19 proc
drwx------   1 root           root             27 Mar  5 02:13 root
drwxr-xr-x   1 root           root            136 Mar  5 02:07 run
lrwxrwxrwx   1 root           root              8 Jan 26 02:05 sbin -> usr/sbin
drwxr-xr-x   2 root           root              6 Jan 26 02:05 srv
dr-xr-xr-x  13 root           root              0 Mar 14 01:19 sys
drwxrwxrwt   1 root           root             29 Mar  5 02:13 tmp
drwxr-xr-x   1 root           root             26 Jan 26 02:05 usr
drwxr-xr-x   1 root           root             25 Jan 26 02:13 var
drwxr-xr-x   4 alestd-picoctf alestd-picoctf   80 Mar  5 02:13 wine
alestd-picoctf@webshell:/$ cd
alestd-picoctf@webshell:~$ ls
Addadshashanammu        code.py       fixme1.py            level3.hash.bin
Addadshashanammu.zip    codebook.txt  fixme2.py            level3.py
Addadshashanammu.zip.1  convertme.py  level1.flag.txt.enc  runme.py
README.txt              drop-in       level1.py            serpentine.py
]                       enc_flag      level2.flag.txt.enc  static
big-zip-files.zip       files         level2.py            strings
challenge.zip           files.zip     level3.flag.txt.enc
alestd-picoctf@webshell:~$ cd /drop-in
-bash: cd: /drop-in: No such file or directory
alestd-picoctf@webshell:~$ cd drop-in/
alestd-picoctf@webshell:~/drop-in$ ls -al
total 12
drwxr-xr-x 3 alestd-picoctf alestd-picoctf   49 Mar 12  2024 .
drwxr-xr-x 7 alestd-picoctf alestd-picoctf 4096 Mar 14 01:54 ..
drwxr-xr-x 8 alestd-picoctf alestd-picoctf 4096 Mar 12  2024 .git
-rw-r--r-- 1 alestd-picoctf alestd-picoctf   11 Mar 12  2024 message.txt
alestd-picoctf@webshell:~/drop-in$ cat message.txt
TOP SECRET
alestd-picoctf@webshell:~/drop-in$ git reflog

[1]+  Stopped                 git reflog
alestd-picoctf@webshell:~/drop-in$ 
alestd-picoctf@webshell:~/drop-in$ git checkout b562f0b
Note: switching to 'b562f0b'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at b562f0b create flag
alestd-picoctf@webshell:~/drop-in$ ls
message.txt
alestd-picoctf@webshell:~/drop-in$ cat message.txt
picoCTF{s@n1t1z3_c785c319}

```