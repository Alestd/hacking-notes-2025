#### Description

The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).


#  Solución 


````

┌──(kali㉿kali)-[~/src]
└─$ nano main.rs
                                                                                        
┌──(kali㉿kali)-[~/src]
└─$ cargo build     
   Compiling rust_proj v0.1.0 (/home/kali)
error[E0308]: mismatched types
  --> src/main.rs:35:31
   |
35 |     decrypt(encrypted_buffer, &party_foul); // Is this the correct way to pass a...
   |     -------                   ^^^^^^^^^^^ types differ in mutability
   |     |
   |     arguments to this function are incorrect
   |
   = note: expected mutable reference `&mut String`
                      found reference `&String`
note: function defined here
  --> src/main.rs:3:4
   |
3  | fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we...
   |    ^^^^^^^                           ----------------------------

For more information about this error, try `rustc --explain E0308`.
error: could not compile `rust_proj` (bin "rust_proj") due to 1 previous error
                                                                                        
┌──(kali㉿kali)-[~/src]
└─$ nano main.rs
                                                                                        
┌──(kali㉿kali)-[~/src]
└─$ cargo build 
   Compiling rust_proj v0.1.0 (/home/kali)
error[E0596]: cannot borrow `party_foul` as mutable, as it is not declared as mutable
  --> src/main.rs:35:31
   |
35 |     decrypt(encrypted_buffer, &mut party_foul); // Is this the correct way to pa...
   |                               ^^^^^^^^^^^^^^^ cannot borrow as mutable
   |
help: consider changing this to be mutable
   |
34 |     let mut party_foul = String::from("Using memory unsafe languages is a: "); // Is this variable changeable?
   |         +++

For more information about this error, try `rustc --explain E0596`.
error: could not compile `rust_proj` (bin "rust_proj") due to 1 previous error
                                                                                        
┌──(kali㉿kali)-[~/src]
└─$ nano main.rs
                                                                                        
┌──(kali㉿kali)-[~/src]
└─$ cargo build 
   Compiling rust_proj v0.1.0 (/home/kali)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 1.80s
                                                                                        
┌──(kali㉿kali)-[~/src]
└─$ cargo run  
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.06s
     Running `/home/kali/target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}


```