## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

## Pistas

1. To view the file in the webshell, do: `$ nano level1.py`
2. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
3. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución
`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py`
`--2025-02-21 07:50:51--  https://artifacts.picoctf.net/c/11/level1.py`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.93, 3.160.5.42, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 876 [application/octet-stream]`
`Saving to: 'level1.py'`

`level1.py                                100%[===============================================================================>]     876  --.-KB/s    in 0s`      

`2025-02-21 07:50:51 (46.0 MB/s) - 'level1.py' saved [876/876]`

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc`
`--2025-02-21 07:51:07--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.42, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 30 [application/octet-stream]`
`Saving to: 'level1.flag.txt.enc'`

`level1.flag.txt.enc                      100%[===============================================================================>]      30  --.-KB/s    in 0s`      

`2025-02-21 07:51:07 (115 KB/s) - 'level1.flag.txt.enc' saved [30/30]`

`OmarSC-picoctf@webshell:~$ nano level1.py`
`OmarSC-picoctf@webshell:~$ python3 level1.py`
`Please enter correct password for flag: 1e1a`
`Welcome back... your flag, user:`
`picoCTF{545h_r1ng1ng_fa343060}`
`OmarSC-picoctf@webshell:~$` `



## Notas Adicionales

La bandera se encontraba en el usuario a la hora de abrir con el nano el archivo de `"level1.py"`

## Referencias
- 