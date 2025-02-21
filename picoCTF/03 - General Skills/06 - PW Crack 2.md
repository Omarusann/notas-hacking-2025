## Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## Pistas

1. Does that encoding look familiar?
2. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py`
`--2025-02-21 07:55:28--  https://artifacts.picoctf.net/c/15/level2.py`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.18, 3.160.5.71, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 914 [application/octet-stream]`
`Saving to: 'level2.py'`

`level2.py                                100%[===============================================================================>]     914  --.-KB/s    in 0s`      

`2025-02-21 07:55:29 (955 MB/s) - 'level2.py' saved [914/914]`

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc`
`--2025-02-21 07:55:37--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.42, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 31 [application/octet-stream]`
`Saving to: 'level2.flag.txt.enc'`

`level2.flag.txt.enc                      100%[===============================================================================>]      31  --.-KB/s    in 0s`      

`2025-02-21 07:55:38 (2.40 MB/s) - 'level2.flag.txt.enc' saved [31/31]`

`OmarSC-picoctf@webshell:~$ nano level2.py`
`OmarSC-picoctf@webshell:~$ python3 level2.py`
`Please enter correct password for flag: 39ce`
`Welcome back... your flag, user:`
`picoCTF{tr45h_51ng1ng_502ec42e}`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales

La bandera estaba encriptada en HEX, entonces solo se necesitaba desencriptar el asunto

## Referencias
- CyberChef