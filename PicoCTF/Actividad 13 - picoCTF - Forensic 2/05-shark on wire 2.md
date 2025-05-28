#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

# Solución

````
└─$ wget https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap
--2025-05-27 20:02:55--  https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 112318 (110K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                              100%[====================================================================================>] 109.69K   661KB/s    in 0.2s    

2025-05-27 20:02:56 (661 KB/s) - ‘capture.pcap’ saved [112318/112318]

                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ nano exp.py
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ nano exp.py
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ python3 -m pip install scapy
Collecting scapy
  Downloading scapy-2.6.1-py3-none-any.whl.metadata (5.6 kB)
Downloading scapy-2.6.1-py3-none-any.whl (2.4 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.4/2.4 MB 9.3 MB/s eta 0:00:00
Installing collected packages: scapy
Successfully installed scapy-2.6.1
                                                                                                                                                                       
┌──(venv)─(kali㉿kali)-[~]
└─$ python3 exp.py

picoCTF{p1LLf3r3d_data_v1a_st3g0}



```