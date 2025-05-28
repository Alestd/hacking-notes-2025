We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag


````
Abrir el paquete en wireshark, en editar->preferencias y buscar el protocolo TLS para editar la llave con la llave que descargamos, ahora descargamos vulture.jpg de un paquete.

┌──(venv)─(kali㉿kali)-[~]
└─$ strings vulture.jpg -n15 
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz


```