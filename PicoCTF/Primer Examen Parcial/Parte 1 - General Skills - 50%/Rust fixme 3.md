#### Description

Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag! Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/dcdaf491b35c1d0f5075e9583edbbb7aaea1dffb6ad32bc000e4d87b5200ff7b/fixme3.tar.gz).

# Solución


````

┌──(kali㉿kali)-[~/pico]
└─$ wget https://challenge-files.picoctf.net/c_verbal_sleep/dcdaf491b35c1d0f5075e9583edbbb7aaea1dffb6ad32bc000e4d87b5200ff7b/fixme3.tar.gz
--2025-04-16 20:30:05--  https://challenge-files.picoctf.net/c_verbal_sleep/dcdaf491b35c1d0f5075e9583edbbb7aaea1dffb6ad32bc000e4d87b5200ff7b/fixme3.tar.gz
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 65.9.149.24, 65.9.149.85, 65.9.149.59, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|65.9.149.24|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1776 (1.7K) [application/octet-stream]
Saving to: ‘fixme3.tar.gz’

fixme3.tar.gz         100%[=========================>]   1.73K  --.-KB/s    in 0s      

2025-04-16 20:30:05 (38.4 MB/s) - ‘fixme3.tar.gz’ saved [1776/1776]

                                                                                        
┌──(kali㉿kali)-[~/pico]
└─$ tar -xvzf fixme3.tar.gz
fixme3/
fixme3/Cargo.toml
fixme3/Cargo.lock
fixme3/src/
fixme3/src/main.rs
                                                                                        
┌──(kali㉿kali)-[~/pico]
└─$ cd fixme3
                                                                                        
┌──(kali㉿kali)-[~/pico/fixme3]
└─$ cargo build
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/kali/pico/fixme3)
error[E0133]: call to unsafe function `std::slice::from_raw_parts` is unsafe and requires unsafe function or block
  --> src/main.rs:31:31
   |
31 | ..._slice = std::slice::from_raw_parts(decrypted_ptr, decrypted_len);
   |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ call to unsafe function                                                                               
   |
   = note: consult the function's documentation for information on how to avoid undefined behavior

For more information about this error, try `rustc --explain E0133`.
error: could not compile `rust_proj` (bin "rust_proj") due to 1 previous error
                                                                                        
┌──(kali㉿kali)-[~/pico/fixme3]
└─$ cd src     
                                                                                        
┌──(kali㉿kali)-[~/pico/fixme3/src]
└─$ nano main.rs
                                                                                        
┌──(kali㉿kali)-[~/pico/fixme3/src]
└─$ cargo build 
   Compiling rust_proj v0.1.0 (/home/kali/pico/fixme3)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.67s
                                                                                        
┌──(kali㉿kali)-[~/pico/fixme3/src]
└─$ cargo run
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.02s
     Running `/home/kali/pico/fixme3/target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{n0w_y0uv3_f1x3d_1h3m_411}


```
