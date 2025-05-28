#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

# Solución

````
Abrir el paquete en wireshark, en editar->preferencias y buscar el protocolo TLS para editar la llave con la llave que descargamos y ahora buscamos en edit->find en detalles de paquetes una cadena "picoCTF"

picoCTF{nongshim.shrimp.crackers}


```