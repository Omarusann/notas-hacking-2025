## Descripción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.

## Pistas

1. Remember the flag format is picoCTF{XXXX}
2. What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)


## Solución

`OmarSC-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 7480 > datos`
`^C`
`OmarSC-picoctf@webshell:~$ cat datos | grep pico`
`picoCTF{digital_plumb3r_06e9d954}`


### Solucion 2

`OmarSC-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 7480 | grep pico`
`picoCTF{digital_plumb3r_06e9d954}`



## Notas Adicionales

- Se guarda el archivo o se filtra directamente con el `grep`

## Referencias
- https://www.linfo.org/pipes.html

