
#### Description

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py) using [this password](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/pw.txt) to get [the flag](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/flag.txt.en)?

#### Hints 

1.-Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py`

# Solución 

```

alestd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py
--2025-04-16 01:51:10--  https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1328 (1.3K) [application/octet-stream]
Saving to: 'ende.py'

ende.py                                         100%[=====================================================================================================>]   1.30K  --.-KB/s    in 0s      

2025-04-16 01:51:10 (1.10 GB/s) - 'ende.py' saved [1328/1328]

alestd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/flag.txt.en
--2025-04-16 01:51:33--  https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/flag.txt.en
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 140 [application/octet-stream]
Saving to: 'flag.txt.en'

flag.txt.en                                     100%[=====================================================================================================>]     140  --.-KB/s    in 0s      

2025-04-16 01:51:33 (88.2 MB/s) - 'flag.txt.en' saved [140/140]

alestd-picoctf@webshell:~$ ls -l
total 16
-rw-r--r-- 1 root           root           4443 Apr 16 01:48 README.txt
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf 1328 Mar 16  2021 ende.py
-rw-rw-r-- 1 alestd-picoctf alestd-picoctf  140 Mar 16  2021 flag.txt.en
alestd-picoctf@webshell:~$ python3 ende.py -d flag.txt.en
Please enter the password:6008014f6008014f6008014f6008014f
picoCTF{4p0110_1n_7h3_h0us3_6008014f}


```