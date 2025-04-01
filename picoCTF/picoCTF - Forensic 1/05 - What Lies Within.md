## Descripción

There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
## Pistas

1. There is data encoded somewhere... there might be an online decoder.

## Solución

`OmarSC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png`
`--2025-04-01 18:57:15--  https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 625219 (611K) [application/octet-stream]`
`Saving to: 'buildings.png'`

`buildings.png       100%[==================>] 610.57K  1.86MB/s    in 0.3s`    

`2025-04-01 18:57:15 (1.86 MB/s) - 'buildings.png' saved [625219/625219]`

`OmarSC-picoctf@webshell:~$` 
`PCOmar:~# sudo gem install zsteg`
`PCOmar:~# zsteg -a buildings.png`
`picoCTF{h1d1ng_1n_th3_b1t5}`
`PCOmar:~#`


`O podemos acceder a la pagina de https://stylesuxx.github.io/steganography/, cargar la imagen y darle en decode`

`picoCTF{h1d1ng_1n_th3_b1t5}`
## Notas Adicionales



## Referencias
- 

