## Descripción

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)
## Pistas

1. (None)

## Solución

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ wget https://artifacts.picoctf.net/c/214/disk.flag.img.gz`
`--2025-05-08 13:12:55--  https://artifacts.picoctf.net/c/214/disk.flag.img.gz`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.64, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 44360927 (42M) [application/octet-stream]`
`Saving to: ‘disk.flag.img.gz.1’`

`disk.flag.img.gz.1               100%[==========================================================>]  42.31M  8.85MB/s    in 4.9s`    

`2025-05-08 13:13:08 (8.72 MB/s) - ‘disk.flag.img.gz.1’ saved [44360927/44360927]`


`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ ls`    
`disk.flag.img.gz  disk.flag.img.gz.1`

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ gunzip disk.flag.img.gz` 

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ ls`
`disk.flag.img  disk.flag.img.gz.1`

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ mmls disk.flag.img`         
`DOS Partition Table`
`Offset Sector: 0`
`Units are in 512-byte sectors`

      `Slot      Start        End          Length       Description`
`000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)`
`001:  -------   0000000000   0000002047   0000002048   Unallocated`
`002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)`
`003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)`
`004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)`

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ fls -o 411648 disk.flag.img`
`d/d 460:        home`
`d/d 11: lost+found`
`d/d 12: boot`
`d/d 13: etc`
`d/d 81: proc`
`d/d 82: dev`
`d/d 83: tmp`
`d/d 84: lib`
`d/d 87: var`
`d/d 96: usr`
`d/d 106:        bin`
`d/d 120:        sbin`
`d/d 466:        media`
`d/d 470:        mnt`
`d/d 471:        opt`
`d/d 472:        root`
`d/d 473:        run`
`d/d 475:        srv`
`d/d 476:        sys`
`d/d 2041:       swap`
`V/V 51001:      $OrphanFiles`

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ fls -o 411648 disk.flag.img 472`
`r/r 1875:       .ash_history`
`r/r * 1876(realloc):    flag.txt`
`r/r 1782:       flag.txt.enc`

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ strings -t d disk.flag.img | grep -iE "flag.txt"`
`218985524 flag.txt`
`218985540 flag.txt.enc`
`219964416 touch flag.txt`
`219964431 nano flag.txt` 
`219964483 nano flag.txt` 
`219964506 openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567`
`219964588 shred -u flag.txt`
`303193140 flag.txt`
`303317044 flag.txt`
`303317060 flag.txt.enc`
`303328308 flag.txt`
`303328324 flag.txt.enc`

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ strings -t d disk.flag.img | grep -iE "Salted"`  
`221247488 Salted__S`
`311007912 Salted__`
`320331880 openssl enc'd data with salted password, base64 encoded`
`320920944 Salted__`
`320921072 openssl enc'd data with salted password`
`325069856 salted -`
`325071360 salted & iterated -`
`326442256 Salted S2K`
`326442632 Salted&Iterated S2K`

`┌──(kali㉿kali)-[~/Desktop/forensic4/operationOrchid]`
`└─$ openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567; cat flag.txt`

`picoCTF{h4un71ng_p457_1d02081e}`


## Notas Adicionales



## Referencias
- 

