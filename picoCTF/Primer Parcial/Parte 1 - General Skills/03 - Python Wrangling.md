## Descripción

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py) using [this password](https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/pw.txt) to get [the flag](https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/flag.txt.en)?
## Pistas

1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py`
2. `$ man python`

## Solución


`OmarSC-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py`
`--2025-04-16 19:56:35--  https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 1328 (1.3K) [application/octet-stream]`
`Saving to: 'ende.py'`

`ende.py                                   100%[===================================================================================>]   1.30K  --.-KB/s    in 0s`      

`2025-04-16 19:56:35 (603 MB/s) - 'ende.py' saved [1328/1328]`

`OmarSC-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/flag.txt.en`
`--2025-04-16 19:57:28--  https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/flag.txt.en`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 140 [application/octet-stream]`
`Saving to: 'flag.txt.en'`

`flag.txt.en                               100%[===================================================================================>]     140  --.-KB/s    in 0s`      

`2025-04-16 19:57:28 (55.0 MB/s) - 'flag.txt.en' saved [140/140]`

`OmarSC-picoctf@webshell:~$ ls`
`README.txt  ende.py  flag.txt.en  server.py`
`OmarSC-picoctf@webshell:~$ man python`     
`OmarSC-picoctf@webshell:~$ python ende.py` 
`Usage: ende.py (-e/-d) [file]`
`OmarSC-picoctf@webshell:~$ python ende.py  -h`
`Usage: ende.py (-e/-d) [file]`
`Examples:`
  `To decrypt a file named 'pole.txt', do: '$ python ende.py -d pole.txt'`

`OmarSC-picoctf@webshell:~$ python ende.py -d flag.txt.en`
`Please enter the password:dbd1bea4dbd1bea4dbd1bea4dbd1bea4`
`picoCTF{4p0110_1n_7h3_h0us3_dbd1bea4}`
`OmarSC-picoctf@webshell:~$` 

## Notas Adicionales



## Referencias
- 

