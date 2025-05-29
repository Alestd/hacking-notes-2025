#### Description

Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

# Solución 

````
└─$ wget https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
--2025-05-28 18:48:42--  https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Report_for_ABC_Labs.pdf         100%[===================================================================================>]  34.10K  --.-KB/s    in 0.04s   

2025-05-28 18:48:42 (778 KB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]

                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ sudo apt install poppler-utils
[sudo] password for kali: 
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Upgrading:
  libgpgme11t64  libgpgmepp6t64  libpng16-16t64  libpoppler-glib8t64  python3-gpg
                                                                                                                                                                      
Installing:
  poppler-utils
                                                                                                                                                                      
Installing dependencies:
  libpoppler145
                                                                                                                                                                      
Summary:
  Upgrading: 5, Installing: 2, Removing: 0, Not Upgrading: 1469
  Download size: 621 kB / 3,753 kB
  Space needed: 4,810 kB / 58.4 GB available

Continue? [Y/n] y
Err:1 http://http.kali.org/kali kali-rolling/main amd64 poppler-utils amd64 25.01.0-5
  404  Not Found [IP: 54.39.128.230 80]
Get:2 http://http.kali.org/kali kali-rolling/main amd64 python3-gpg amd64 1.24.2-1+b1 [408 kB]
Fetched 408 kB in 1s (803 kB/s)      
Error: Failed to fetch http://http.kali.org/kali/pool/main/p/poppler/poppler-utils_25.01.0-5_amd64.deb  404  Not Found [IP: 54.39.128.230 80]
Error: Unable to fetch some archives, maybe run apt-get update or try with --fix-missing?
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ pdftotext Financial_Report_for_ABC_Labs.pdf
Command 'pdftotext' not found, but can be installed with:
sudo apt install poppler-utils
Do you want to install it? (N/y)y
sudo apt install poppler-utils
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Upgrading:
  libgpgme11t64  libgpgmepp6t64  libpng16-16t64  libpoppler-glib8t64  python3-gpg
                                                                                                                                                                      
Installing:
  poppler-utils
                                                                                                                                                                      
Installing dependencies:
  libpoppler145
                                                                                                                                                                      
Summary:
  Upgrading: 5, Installing: 2, Removing: 0, Not Upgrading: 1469
  Download size: 213 kB / 3,753 kB
  Space needed: 4,810 kB / 58.4 GB available

Continue? [Y/n] y
Err:1 http://http.kali.org/kali kali-rolling/main amd64 poppler-utils amd64 25.01.0-5
  404  Not Found [IP: 54.39.128.230 80]
Error: Failed to fetch http://http.kali.org/kali/pool/main/p/poppler/poppler-utils_25.01.0-5_amd64.deb  404  Not Found [IP: 54.39.128.230 80]
Error: Unable to fetch some archives, maybe run apt-get update or try with --fix-missing?
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cat Financial_Report_for_ABC_Labs.txt
cat: Financial_Report_for_ABC_Labs.txt: No such file or directory
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ sudo apt install poppler-utils                                           
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Upgrading:
  libgpgme11t64  libgpgmepp6t64  libpng16-16t64  libpoppler-glib8t64  python3-gpg
                                                                                                                                                                      
Installing:
  poppler-utils
                                                                                                                                                                      
Installing dependencies:
  libpoppler145
                                                                                                                                                                      
Summary:
  Upgrading: 5, Installing: 2, Removing: 0, Not Upgrading: 1469
  Download size: 213 kB / 3,753 kB
  Space needed: 4,810 kB / 58.4 GB available

Continue? [Y/n] n
Abort.
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ pdftotext Financial_Report_for_ABC_Labs.pdf                              
Command 'pdftotext' not found, but can be installed with:
sudo apt install poppler-utils
Do you want to install it? (N/y)y
sudo apt install poppler-utils
The following packages were automatically installed and are no longer required:
  libgit2-1.8        libmbedcrypto16  libmbedx509-7      lld-19      python3.12-dev      python3.12-venv
  libhttp-parser2.9  libmbedtls21     libpython3.12-dev  python3.12  python3.12-minimal  rust-llvm
Use 'sudo apt autoremove' to remove them.

Upgrading:
  libgpgme11t64  libgpgmepp6t64  libpng16-16t64  libpoppler-glib8t64  python3-gpg
                                                                                                                                                                      
Installing:
  poppler-utils
                                                                                                                                                                      
Installing dependencies:
  libpoppler145
                                                                                                                                                                      
Summary:
  Upgrading: 5, Installing: 2, Removing: 0, Not Upgrading: 1469
  Download size: 213 kB / 3,753 kB
  Space needed: 4,810 kB / 58.4 GB available
  
cat Financial_Report_for_ABC_Labs.txt
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.

Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.

picoCTF{C4n_Y0u_S33_m3_fully}

```