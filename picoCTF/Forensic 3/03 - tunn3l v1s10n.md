## Descripción

We found this [file](https://mercury.picoctf.net/static/09a86202e72dbdb5bf4d1b5d2c6a5b86/tunn3l_v1s10n). Recover the flag.
## Pistas

1. Weird that it won't display right...

## Solución

`┌──(kali㉿kali)-[~/Desktop/forensic3/tunel]`
`└─$ wget https://mercury.picoctf.net/static/09a86202e72dbdb5bf4d1b5d2c6a5b86/tunn3l_v1s10n`
`--2025-05-06 14:51:20--  https://mercury.picoctf.net/static/09a86202e72dbdb5bf4d1b5d2c6a5b86/tunn3l_v1s10n`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 2893454 (2.8M) [application/octet-stream]`
`Saving to: ‘tunn3l_v1s10n’`

`tunn3l_v1s10n                                              100%[========================================================================================================================================>]   2.76M   382KB/s    in 8.4s`    

`2025-05-06 14:51:31 (335 KB/s) - ‘tunn3l_v1s10n’ saved [2893454/2893454]`


`┌──(kali㉿kali)-[~/Desktop/forensic3/tunel]`
`└─$ xxd -l 100 tunn3l_v1s10n` 
`00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........`
`00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........`
`00000020: 0000 5826 2c00 2516 0000 2516 0000 0000  ..X&,.%...%.....`
`00000030: 0000 0000 0000 231a 1727 1e1b 2920 1d2a  ......#..'..) .*`
`00000040: 211e 261d 1a31 2825 352c 2933 2a27 382f  !.&..1(%5,)3*'8/`
`00000050: 2c2f 2623 332a 262d 2420 3b32 2e32 2925  ,/&#3*&-$ ;2.2)%`
`00000060: 3027 2333                                0'#3`

`┌──(kali㉿kali)-[~/Desktop/forensic3/tunel]`
`└─$ cp tunn3l_v1s10n flag.bmp`

`┌──(kali㉿kali)-[~/Desktop/forensic3/tunel]`
`└─$ hexeditor flag.bmp`                                                                         

`┌──(kali㉿kali)-[~/Desktop/forensic3/tunel]`
`└─$ hexeditor flag.bmp`

`┌──(kali㉿kali)-[~/Desktop/forensic3/tunel]`
`└─$ eog flag.bmp` 


picoCTF{qu1t3_a_v13w_2020}
## Notas Adicionales



## Referencias
- 

