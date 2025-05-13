## Descripción

Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/260/flag.png).
## Pistas

1. (None)

## Solución

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/hideMe]`
`└─$ wget https://artifacts.picoctf.net/c/260/flag.png`          
`--2025-05-13 03:30:32--  https://artifacts.picoctf.net/c/260/flag.png`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.26, 3.161.55.64, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 43005 (42K) [application/octet-stream]`
`Saving to: ‘flag.png’`

`flag.png                         100%[=========================================================>]  42.00K  --.-KB/s    in 0.06s`   

`2025-05-13 03:30:33 (716 KB/s) - ‘flag.png’ saved [43005/43005]`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/hideMe]`
`└─$ binwalk -e flag.png`                

`DECIMAL       HEXADECIMAL     DESCRIPTION`
--------------------------------------------------------------------------------
`41            0x29            Zlib compressed data, compressed`
`39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/`
`39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2944, uncompressed size: 3095, name: secret/flag.png`

`WARNING: One or more files failed to extract: either no utility was found or it's unimplemented`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/hideMe]`
`└─$ ls` 
`flag.png  _flag.png.extracted`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/hideMe]`
`└─$ cd _flag.png.extracted/secret` 

`┌──(kali㉿kali)-[~/…/tarea3Forensic/hideMe/_flag.png.extracted/secret]`
`└─$ ls`
`flag.png`

`┌──(kali㉿kali)-[~/…/tarea3Forensic/hideMe/_flag.png.extracted/secret]`
`└─$ open flag.png` 

`┌──(kali㉿kali)-[~/…/tarea3Forensic/hideMe/_flag.png.extracted/secret]`
`└─$` 


`picoCTF{Hiddinng_An_imag3_within_@n_ima9e_ad9f6587}`

## Notas Adicionales



## Referencias
- 

