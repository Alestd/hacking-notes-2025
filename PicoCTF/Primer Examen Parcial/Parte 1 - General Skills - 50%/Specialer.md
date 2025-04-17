
#### Description

Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 49249 ctf-player@saturn.picoctf.net`. The password is `d137d16e`


# Solución 

````

alestd-picoctf@webshell:~$ ssh -p 49249 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:49249 ([13.59.203.175]:49249)' can't be established.
ED25519 key fingerprint is SHA256:lMXKIC17ONzyUJx7ZYBY5VSwoxCz20uq5/Nm+IhXKew.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:49249' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password: 
Specialer$ echo "$(<ala/kazam.tet)"
-bash: ala/kazam.tet: No such file or directory

Specialer$ help
GNU bash, version 5.0.17(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                                    history [-c] [-d offset] [n] or history -anr>
 (( expression ))                                if COMMANDS; then COMMANDS; [ elif COMMANDS;>
 . filename [arguments]                          jobs [-lnprs] [jobspec ...] or jobs -x comma>
 :                                               kill [-s sigspec | -n signum | -sigspec] pid>
 [ arg... ]                                      let arg [arg ...]
 [[ expression ]]                                local [option] name[=value] ...
 alias [-p] [name[=value] ... ]                  logout [n]
 bg [job_spec ...]                               mapfile [-d delim] [-n count] [-O origin] [->
 bind [-lpsvPSVX] [-m keymap] [-f filename] [->  popd [-n] [+N | -N]
 break [n]                                       printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]               pushd [-n] [+N | -N | dir]
 caller [expr]                                   pwd [-LP]
 case WORD in [PATTERN [| PATTERN]...) COMMAND>  read [-ers] [-a array] [-d delim] [-i text] >
 cd [-L|[-P [-e]] [-@]] [dir]                    readarray [-d delim] [-n count] [-O origin] >
 command [-pVv] command [arg ...]                readonly [-aAf] [name[=value] ...] or readon>
 compgen [-abcdefgjksuv] [-o option] [-A actio>  return [n]
 complete [-abcdefgjksuv] [-pr] [-DEI] [-o opt>  select NAME [in WORDS ... ;] do COMMANDS; do>
 compopt [-o|+o option] [-DEI] [name ...]        set [-abefhkmnptuvxBCHP] [-o option-name] [->
 continue [n]                                    shift [n]
 coproc [NAME] command [redirections]            shopt [-pqsu] [-o] [optname ...]
 declare [-aAfFgilnrtux] [-p] [name[=value] ..>  source filename [arguments]
 dirs [-clpv] [+N] [-N]                          suspend [-f]
 disown [-h] [-ar] [jobspec ... | pid ...]       test [expr]
 echo [-neE] [arg ...]                           time [-p] pipeline
 enable [-a] [-dnps] [-f filename] [name ...]    times
 eval [arg ...]                                  trap [-lp] [[arg] signal_spec ...]
 exec [-cl] [-a name] [command [arguments ...]>  true
 exit [n]                                        type [-afptP] name [name ...]
 export [-fn] [name[=value] ...] or export -p    typeset [-aAfFgilnrtux] [-p] name[=value] ..>
 false                                           ulimit [-SHabcdefiklmnpqrstuvxPT] [limit]
 fc [-e ename] [-lnr] [first] [last] or fc -s >  umask [-p] [-S] [mode]
 fg [job_spec]                                   unalias [-a] name [name ...]
 for NAME [in WORDS ... ] ; do COMMANDS; done    unset [-f] [-v] [-n] [name ...]
 for (( exp1; exp2; exp3 )); do COMMANDS; done>  until COMMANDS; do COMMANDS; done
 function name { COMMANDS ; } or name () { COM>  variables - Names and meanings of some shell>
 getopts optstring name [arg]                    wait [-fn] [id ...]
 hash [-lr] [-p pathname] [-dt] [name ...]       while COMMANDS; do COMMANDS; done
 help [-dms] [pattern ...]                       { COMMANDS ; }
Specialer$ echo *                  
abra ala sim
Specialer$ echo */*
abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt
Specialer$ echo "$(<ala/kazam.tet)"
-bash: ala/kazam.tet: No such file or directory

Specialer$ echo */*
abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt
Specialer$ echo "$(<abra/cadabra.tet)"
-bash: abra/cadabra.tet: No such file or directory

Specialer$ echo "$(<abra/cadabra.txt)"
Nothing up my sleeve!
Specialer$ echo "$(<ala/kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_838b49d1}



```