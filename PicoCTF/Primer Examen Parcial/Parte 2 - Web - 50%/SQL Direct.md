#### Description

Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 54607 -U postgres pico`Password is `postgres`


# Solución

````
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 54607 -U postgres pico
Password for user postgres: 
psql (17.0 (Debian 17.0-1+b2), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \l

zsh: suspended  psql -h saturn.picoctf.net -p 54607 -U postgres pico
                                                                                        
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 54607 -U postgres pico
Password for user postgres: 
psql (17.0 (Debian 17.0-1+b2), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \c pico
psql (17.0 (Debian 17.0-1+b2), server 15.2 (Debian 15.2-1.pgdg110+1))
You are now connected to database "pico" as user "postgres".
pico=# \dt 
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# selec * from flags;
ERROR:  syntax error at or near "selec"
LINE 1: selec * from flags;
        ^
pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)



```