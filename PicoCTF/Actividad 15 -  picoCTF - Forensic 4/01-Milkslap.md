http://mercury.picoctf.net:58537/


# Solución 

````
└─$ wget http://mercury.picoctf.net:58537/                                                            
--2025-05-28 10:27:01--  http://mercury.picoctf.net:58537/
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:58537... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: ‘index.html’

index.html                                    [ <=>                                                                                ]     517  --.-KB/s    in 0s      

2025-05-28 10:27:01 (41.3 MB/s) - ‘index.html’ saved [517]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ sudo apt install ruby-rubygems
[sudo] password for kali: 
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Upgrading:
  bundler  ruby-bundler  ruby-rubygems

Summary:
  Upgrading: 3, Installing: 0, Removing: 0, Not Upgrading: 1474
  Download size: 0 B / 922 kB
  Space needed: 721 kB / 58.9 GB available

Continue? [Y/n] y
(Reading database ... 405763 files and directories currently installed.)
Preparing to unpack .../bundler_2.6.3-1_all.deb ...
Unpacking bundler (2.6.3-1) over (2.4.20-1) ...
Preparing to unpack .../ruby-bundler_2.6.3-1_all.deb ...
Unpacking ruby-bundler (2.6.3-1) over (2.4.20-1) ...
Preparing to unpack .../ruby-rubygems_3.6.3-1_all.deb ...
Unpacking ruby-rubygems (3.6.3-1) over (3.4.20-1) ...
Setting up ruby-rubygems (3.6.3-1) ...
Setting up ruby-bundler (2.6.3-1) ...
Setting up bundler (2.6.3-1) ...
Processing triggers for kali-menu (2024.4.0) ...
Processing triggers for man-db (2.13.0-1) ...
                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ gem install zsteg
Fetching rainbow-3.1.1.gem
Fetching zsteg-0.2.13.gem
Fetching zpng-0.4.5.gem
Fetching iostruct-0.5.0.gem
Defaulting to user installation because default installation directory (/var/lib/gems/3.1.0) is not writable.
Successfully installed rainbow-3.1.1
Defaulting to user installation because default installation directory (/var/lib/gems/3.1.0) is not writable.
WARNING:  You don't have /home/kali/.local/share/gem/ruby/3.1.0/bin in your PATH,
          gem executables (zpng) will not run.
Successfully installed zpng-0.4.5
Defaulting to user installation because default installation directory (/var/lib/gems/3.1.0) is not writable.
Successfully installed iostruct-0.5.0
Defaulting to user installation because default installation directory (/var/lib/gems/3.1.0) is not writable.
WARNING:  You don't have /home/kali/.local/share/gem/ruby/3.1.0/bin in your PATH,
          gem executables (zsteg, zsteg-mask, zsteg-reflow) will not run.
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.5.0
Installing ri documentation for iostruct-0.5.0
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 2 seconds
4 gems installed
                                                                                                                                                                      
┌──(kali㉿kali)-[~/ppt/slideMasters]
└─$ zsteg concat_v.png


picoCTF{imag3_m4n1pul4t10n_sl4p5}



```