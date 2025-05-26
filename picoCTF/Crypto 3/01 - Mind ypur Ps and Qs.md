## Descripción

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values)
## Pistas

1. Bits are expensive, I used only a little bit over 100 to save money

## Solución

`┌──(kali㉿kali)-[~/Desktop/Crypto3/mypaq]`
`└─$ wget https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values`    
`--2025-05-26 16:25:51--  https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 205 [application/octet-stream]`
`Saving to: ‘values’`

`values                           100%[=========================================================>]     205  --.-KB/s    in 0s`      

`2025-05-26 16:25:51 (208 MB/s) - ‘values’ saved [205/205]`


`┌──(kali㉿kali)-[~/Desktop/Crypto3/mypaq]`
`└─$ ls`
`values`

`┌──(kali㉿kali)-[~/Desktop/Crypto3/mypaq]`
`└─$ cat values`    
`Decrypt my super sick RSA:`
`c: 421345306292040663864066688931456845278496274597031632020995583473619804626233684`
`n: 631371953793368771804570727896887140714495090919073481680274581226742748040342637`
`e: 65537`                                                                                                                                   
`┌──(kali㉿kali)-[~/Desktop/Crypto3/mypaq]`
`└─$ python`            
`Python 3.12.7 (main, Nov  8 2024, 17:55:36) [GCC 14.2.0] on linux`
`Type "help", "copyright", "credits" or "license" for more information.`

`https://www.dcode.fr/rsa-cipher`
`picoCTF{sma11_N_n0_g0od_55304594}`

## Notas Adicionales



## Referencias
- 

