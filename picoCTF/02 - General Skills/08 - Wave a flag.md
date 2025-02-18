## Descripción

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...
## Pistas

1. This program will only work in the webshell or another Linux computer.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm`
3. Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
4. -h and --help are the most common arguments to give to programs to get more information from them!
5. Not every program implements help features like -h and --help.

## Solución

`OmarSC-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm`
`--2025-02-18 18:24:22--  https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 10936 (11K) [application/octet-stream]`
`Saving to: 'warm'`

`warm                100%[=================>]  10.68K  --.-KB/s    in 0s`      

`2025-02-18 18:24:22 (337 MB/s) - 'warm' saved [10936/10936]`

`OmarSC-picoctf@webshell:~$ file warm`
`warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=506b7be935d8940c672ab0d40d2e03ebd746155b, with debug_info, not stripped`
`OmarSC-picoctf@webshell:~$ chmod +x warm`
`OmarSC-picoctf@webshell:~$ ls`
`README.txt         big-zip-files.zip.1  datos      flag`
`big-zip-files      big-zip-files.zip.2  file       hola`
`big-zip-files.zip  big-zip-files.zip.3  files.zip  warm`
`OmarSC-picoctf@webshell:~$ ./warm -h`
`Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}`
`OmarSC-picoctf@webshell:~$` 

## Notas Adicionales



## Referencias
- 

