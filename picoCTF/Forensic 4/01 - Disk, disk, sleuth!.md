## Descripción

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/ac394d24f88e51a09cc909687cf6d853/dds1-alpine.flag.img.gz)
## Pistas

1. Have you ever used `file` to determine what a file was?
2. Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
3. Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
4. Using your own computer, you could use qemu to boot from this disk!

## Solución

`┌──(kali㉿kali)-[~/Desktop/forensic4/diskDisk]`
`└─$ wget https://mercury.picoctf.net/static/ac394d24f88e51a09cc909687cf6d853/dds1-alpine.flag.img.gz`
`--2025-05-08 12:32:45--  https://mercury.picoctf.net/static/ac394d24f88e51a09cc909687cf6d853/dds1-alpine.flag.img.gz`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 29768910 (28M) [application/octet-stream]`
`Saving to: ‘dds1-alpine.flag.img.gz’`

`dds1-alpine.flag.img.gz          100%[==========================================================>]  28.39M  3.50MB/s    in 6.8s`    

`2025-05-08 12:33:01 (4.17 MB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]`


`┌──(kali㉿kali)-[~/Desktop/forensic4/diskDisk]`
`└─$ gunzip dds1-alpine.flag.img.gz` 


`┌──(kali㉿kali)-[~/Desktop/forensic4/diskDisk]`
`└─$` 

`┌──(kali㉿kali)-[~/Desktop/forensic4/diskDisk]`
`└─$ srch_strings`                    
`^C`
`┌──(kali㉿kali)-[~/Desktop/forensic4/diskDisk]`
`└─$ srch_strings dds1-alpine.flag.img | grep picoCTF`
  `SAY picoCTF{f0r3ns1c4t0r_n30phyt3_dcbf5942}`

`┌──(kali㉿kali)-[~/Desktop/forensic4/diskDisk]`
`└─$` 



## Notas Adicionales



## Referencias
- 

