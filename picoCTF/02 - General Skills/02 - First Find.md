## Descripción

Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)
## Pistas

(None)

## Solución

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/501/files.zip`
`--2025-02-18 06:21:52--  https://artifacts.picoctf.net/c/501/files.zip`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 3995553 (3.8M) [application/octet-stream]`
`Saving to: 'files.zip'`

`files.zip                                 100%[===================================================================================>]   3.81M  1.80MB/s    in 2.1s`    

`2025-02-18 06:21:54 (1.80 MB/s) - 'files.zip' saved [3995553/3995553]`
`OmarSC-picoctf@webshell:~$ cat files.zip`
`<OmarSC-picoctf@webshell:~$ strings files.zip | grep pico`
`picoCTF{f1nd_15_f457_ab443fd1}`
`OmarSC-picoctf@webshell:~$` 
### Solucion N



## Notas Adicionales

- El comando de strings se debe de ejecutar cuando estamos dentro del cat, si no, cuando estemos afuera no hará nada
- (No se puso todo lo que me salio del cat para que no sea vean muchas cosas "innecesarias")


## Referencias
- 

