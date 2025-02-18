## Descripción

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip)
## Pistas

After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

## Solución
`OmarSC-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip`
`--2025-02-18 18:43:00--  https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 4520 (4.4K) [application/octet-stream]`
`Saving to: 'Addadshashanammu.zip'`

`Addadshashanammu.zi 100%[=================>]   4.41K  --.-KB/s    in 0s`      

`2025-02-18 18:43:00 (2.40 GB/s) - 'Addadshashanammu.zip' saved [4520/4520]`

`OmarSC-picoctf@webshell:~$ file Addadshashanammu.zip` 
`Addadshashanammu.zip: Zip archive data, at least v1.0 to extract, compression method=store`
`OmarSC-picoctf@webshell:~$` 
`OmarSC-picoctf@webshell:~$ ls`
`Addadshashanammu  Addadshashanammu.zip  big-zip-files`
`OmarSC-picoctf@webshell:~$ cd Addadshashanammu/`
`OmarSC-picoctf@webshell:~/Addadshashanammu$ ls`
`Almurbalarammi`
`OmarSC-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/`
`OmarSC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assur`
`nabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls`
`fang-of-haynekhtnamet`
`OmarSC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assur`
`nabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ file fang-of-haynekhtnamet` 
`fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=fcea24fb5379795a123bb860267d815e889a6d23, not stripped`
`OmarSC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assur`
`nabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet` 
`*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}`
`OmarSC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assur`
`nabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$` 


## Notas Adicionales

- Con el tab se puede autocompletar los archivos, sin necesidad de escribir todo

## Referencias
- 

