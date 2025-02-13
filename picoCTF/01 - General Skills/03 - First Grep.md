## Descripción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.

## Pistas
grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)


## Solución
`OmarSC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file`
`--2025-02-13 18:29:55--  https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 14551 (14K) [application/octet-stream]`
`Saving to: 'file'`

`file                                                      100%[==================================================================================================================================>]  14.21K  --.-KB/s    in 0s`      

`2025-02-13 18:29:55 (380 MB/s) - 'file' saved [14551/14551]`

`OmarSC-picoctf@webshell:~$ cat file | grep pico`
`picoCTF{grep_is_good_to_find_things_5af9d829}`

## Notas Adicionales

El wget nos sirve para que no descarguemos el archivo, ya que con el webshell, descarga el archivo y luego ya solo ponemos cat flag y nos tira la respuesta.

DEspues con el " | grep (palabra)" buscamos la bandera

## Referencias
- 

