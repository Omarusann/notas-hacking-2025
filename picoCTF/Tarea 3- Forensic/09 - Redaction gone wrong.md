## Descripción

Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Pistas

1. How can you be sure of the redaction?

## Solución

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RedactionGoneWrong]`
`└─$ wget https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf`
`--2025-05-13 03:34:34--  https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.61, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 34915 (34K) [application/octet-stream]`
`Saving to: ‘Financial_Report_for_ABC_Labs.pdf’`

`Financial_Report_for_ABC_Labs.pd 100%[=========================================================>]  34.10K  --.-KB/s    in 0.02s`   

`2025-05-13 03:34:35 (1.66 MB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RedactionGoneWrong]`
`└─$ open Financial_Report_for_ABC_Labs.pdf` 

`Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.`
`Breakdown - Just painted over in MS word.`
`Cost Benefit Analysis`
`Credit Debit`
`This is not the flag, keep looking`
`Expenses from the`
`picoCTF{C4n_Y0u_S33_m3_fully}`
`Redacted document.`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RedactionGoneWrong]`
`└─$` 

## Notas Adicionales



## Referencias
- 

