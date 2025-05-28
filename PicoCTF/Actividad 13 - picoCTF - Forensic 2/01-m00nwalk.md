#### Description

Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
# Solución

````
└─$ wget https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav
--2025-05-27 19:45:41--  https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11066998 (11M) [application/octet-stream]
Saving to: ‘message.wav’

message.wav                               100%[====================================================================================>]  10.55M  8.19MB/s    in 1.3s    

2025-05-27 19:45:43 (8.19 MB/s) - ‘message.wav’ saved [11066998/11066998]


file message.wav
message.wav: RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 48000 Hz

cd /opt

sudo python3 setup.py install

cd picoCTF/forense/moonwalk

sstv -d message.wav -o result.png

picoCTF{beep_boop_im_in_space}


```