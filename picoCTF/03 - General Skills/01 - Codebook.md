## Descripción

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)
## Pistas

1. On the webshell, use `ls` to see if both files are in the directory you are in
2. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py`
`--2025-02-21 06:13:32--  https://artifacts.picoctf.net/c/2/code.py`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.18, 3.160.5.42, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 1278 (1.2K) [application/octet-stream]`
`Saving to: 'code.py'`

`code.py             100%[=================>]   1.25K  --.-KB/s    in 0s`      

`2025-02-21 06:13:32 (1.13 GB/s) - 'code.py' saved [1278/1278]`

`OmarSC-picoctf@webshell:~$ tree`
`-bash: tree: command not found`
`OmarSC-picoctf@webshell:~$ ls`
`README.txt  code.py`
`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt`
`--2025-02-21 06:14:21--  https://artifacts.picoctf.net/c/2/codebook.txt`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.42, 3.160.5.93, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 27 [application/octet-stream]`
`Saving to: 'codebook.txt'`

`codebook.txt        100%[=================>]      27  --.-KB/s    in 0s`      

`2025-02-21 06:14:21 (17.0 MB/s) - 'codebook.txt' saved [27/27]`

`OmarSC-picoctf@webshell:~$ ls`
`README.txt  code.py  codebook.txt`
`OmarSC-picoctf@webshell:~$ python3 code.py`
`picoCTF{c0d3b00k_455157_7d102d7a}`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales

Solo era necesario correr el archivo de code.py, quizá no era tan necesario descargar ambos

## Referencias
- 