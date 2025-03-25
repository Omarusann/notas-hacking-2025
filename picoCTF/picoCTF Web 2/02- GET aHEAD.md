## Descripción

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:34561/](http://mercury.picoctf.net:34561/)
## Pistas

1. Maybe you have more than 2 choices
2. Check out tools like Burpsuite to modify your requests and look at the responses

## Solución

`OmarSC-picoctf@webshell:~$ HEAD http://mercury.picoctf.net:34561/index.php?`
`200 OK`
`Content-Type: text/html; charset=UTF-8`
`Client-Date: Tue, 25 Mar 2025 18:12:48 GMT`
`Client-Peer: 18.189.209.142:34561`
`Client-Response-Num: 1`
`Flag: picoCTF{r3j3ct_th3_du4l1ty_8f878508}`

`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales

- Tenemos que darle el "HEAD" y luego ya poner el link que nos da el pico
- GET nos regresaba el background rojo y el POST nos lo daba azul. Ya el HEAD nos dio la flag
## Referencias
- 

