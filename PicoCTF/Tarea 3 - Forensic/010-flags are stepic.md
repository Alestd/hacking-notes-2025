#### Description

A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their messageTry it [here](http://standard-pizzas.picoctf.net:53065/)!

# Solución

````
┌──(kali㉿kali)-[~]
└─$ sudo apt install python3-venv

python3-venv is already the newest version (3.13.1-2).
python3-venv set to manually installed.
The following packages were automatically installed and are no longer required:
  imagemagick-6.q16  libhttp-parser2.9            libmagickcore-6.q16-7t64  libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libgit2-1.8        libmagickcore-6.q16-7-extra  libmagickwand-6.q16-7t64  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 1470
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ python3 -m venv stepic-env

                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ source stepic-env/bin/activate

                                                                                                                                                                      
┌──(stepic-env)─(kali㉿kali)-[~]
└─$ pip install stepic pillow

Collecting stepic
  Downloading stepic-0.5.0.tar.gz (219 kB)
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting pillow
  Downloading pillow-11.2.1-cp313-cp313-manylinux_2_28_x86_64.whl.metadata (8.9 kB)
Downloading pillow-11.2.1-cp313-cp313-manylinux_2_28_x86_64.whl (4.6 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 4.6/4.6 MB 12.4 MB/s eta 0:00:00
Building wheels for collected packages: stepic
  Building wheel for stepic (pyproject.toml) ... done
  Created wheel for stepic: filename=stepic-0.5.0-py3-none-any.whl size=12506 sha256=f41a0f86397f4cc48e92cd39206cd4e2c519a5a971061c3d8557b6f64d664207
  Stored in directory: /home/kali/.cache/pip/wheels/f7/4c/a1/2791c89a230cdc97ab0c5ad4b7893b2b4ad6f71374f4ce8352
Successfully built stepic
Installing collected packages: pillow, stepic
Successfully installed pillow-11.2.1 stepic-0.5.0

┌──(stepic-env)─(kali㉿kali)-[~]
└─$ wget http://standard-pizzas.picoctf.net:53065/flags/upz.png                            
--2025-05-28 20:02:18--  http://standard-pizzas.picoctf.net:53065/flags/upz.png
Resolving standard-pizzas.picoctf.net (standard-pizzas.picoctf.net)... 3.22.195.189
Connecting to standard-pizzas.picoctf.net (standard-pizzas.picoctf.net)|3.22.195.189|:53065... failed: Connection refused.
                                                                                                                                                                      
┌──(stepic-env)─(kali㉿kali)-[~]
└─$ http://standard-pizzas.picoctf.net:59254/flags/upz.png
zsh: no such file or directory: http://standard-pizzas.picoctf.net:59254/flags/upz.png
                                                                                                                                                                      
┌──(stepic-env)─(kali㉿kali)-[~]
└─$ wget http://standard-pizzas.picoctf.net:59254/flags/upz.png
--2025-05-28 20:04:52--  http://standard-pizzas.picoctf.net:59254/flags/upz.png
Resolving standard-pizzas.picoctf.net (standard-pizzas.picoctf.net)... 3.22.195.189
Connecting to standard-pizzas.picoctf.net (standard-pizzas.picoctf.net)|3.22.195.189|:59254... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1788393 (1.7M) [image/png]
Saving to: ‘upz.png’

upz.png                                   100%[===================================================================================>]   1.71M  2.78MB/s    in 0.6s    

2025-05-28 20:04:53 (2.78 MB/s) - ‘upz.png’ saved [1788393/1788393]

                                                                                                                                                                      
┌──(stepic-env)─(kali㉿kali)-[~]
└─$ pip install stepic
Requirement already satisfied: stepic in ./stepic-env/lib/python3.13/site-packages (0.5.0)
Requirement already satisfied: pillow in ./stepic-env/lib/python3.13/site-packages (from stepic) (11.2.1)


┌──(stepic-env)─(kali㉿kali)-[~]
└─$ python3              
Python 3.13.2 (main, Feb  5 2025, 01:23:35) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from PIL import Image
>>> import stepic
>>> im1=Image.open('upz.png')
/home/kali/stepic-env/lib/python3.13/site-packages/PIL/Image.py:3442: DecompressionBombWarning: Image size (150658990 pixels) exceeds limit of 89478485 pixels, could be decompression bomb DOS attack.
  warnings.warn(
>>> s=stepic.decode(im1)
>>> print(s)
picoCTF{fl4g_h45_fl4g57f48d94}



```