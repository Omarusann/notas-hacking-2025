## Descripción

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Pistas

1. Indentation is very meaningful in Python
2. To view the file in the webshell, do: `$ nano fixme1.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/26/fixme1.py`
`--2025-02-21 06:40:26--  https://artifacts.picoctf.net/c/26/fixme1.py`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.18, 3.160.5.71, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 837 [application/octet-stream]`
`Saving to: 'fixme1.py'`

`fixme1.py           100%[=================>]     837  --.-KB/s    in 0s`      

`2025-02-21 06:40:26 (233 MB/s) - 'fixme1.py' saved [837/837]`

`OmarSC-picoctf@webshell:~$ nano fixme1.py`
`OmarSC-picoctf@webshell:~$ python3 fixme1.py`
  `File "/home/OmarSC-picoctf/fixme1.py", line 20`
    `print('That is correct! Here\'s your flag: ' + flag)`
`IndentationError: unexpected indent`
`OmarSC-picoctf@webshell:~$ nano fixme1.py`
`OmarSC-picoctf@webshell:~$ python3 fixme1.py`
`That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales
El error estaba en la identación, había unas partes como en verde que también eliminé, no se si había algo


## Referencias
- 