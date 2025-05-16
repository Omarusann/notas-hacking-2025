## Descripción

The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?
## Pistas

1. The flag is in the format PICOCTF{}

## Solución


`OmarSC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png`
`--2025-05-12 19:21:06--  https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 100721 (98K) [application/octet-stream]`
`Saving to: 'the_numbers.png'`

`the_numbers.png                   100%[==========================================================>]  98.36K  --.-KB/s    in 0.04s`   

`2025-05-12 19:21:06 (2.21 MB/s) - 'the_numbers.png' saved [100721/100721]`

`OmarSC-picoctf@webshell:~$ ls`
`the_numbers.png`

`OmarSC-picoctf@webshell:~$ file the_numbers.png` 
`the_numbers.png: PNG image data, 774 x 433, 8-bit/color RGB, non-interlaced`

`p i c o C T F {THENUMBERSMASON} 16 9 3 15 3 20 6 {20 8 5 14 21 13 2 5 18 19 13 1 19 15 14}`

`picoCTF{THENUMBERSMASON}`

## Notas Adicionales



## Referencias
- 

