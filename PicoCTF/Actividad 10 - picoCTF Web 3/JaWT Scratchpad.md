#### Description

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090

#### Hints 

1.-What is that cookie?
2.-Have you heard of JWT?
# Solución


````
utilizar el cookie editor ver en jwt y tomar el value
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiY2FybG9zIn0.ibA8ZjnNXLYfuOIQWln6-CmmzUhw-bsu3BivkwnNYDk
despues pegarlo en https://jwt.io/ y modificar el usuario por admin (esto no funciono para esta ocacion)
ir a https://github.com/openwall/john

utiliza jhon para sacar la firma del token
ilovepico
modificar el value, guardar y recargar

picoCTF{jawt_was_just_what_you_thought_f859ab2f}


```