## Descripción

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?
## Pistas

[strings](https://linux.die.net/man/1/strings)
## Solución

`OmarSC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings`
`--2025-02-18 19:08:19--  https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 776032 (758K) [application/octet-stream]`
`Saving to: 'strings'`

`strings             100%[=================>] 757.84K  1.85MB/s    in 0.4s`    

`2025-02-18 19:08:20 (1.85 MB/s) - 'strings' saved [776032/776032]`

`OmarSC-picoctf@webshell:~$ strigs strings | grep pico`
`-bash: strigs: command not found`
`OmarSC-picoctf@webshell:~$ strings strings | grep pico`
`picoCTF{5tRIng5_1T_827aee91}`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales



## Referencias
- 


