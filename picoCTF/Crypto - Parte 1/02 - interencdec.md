## Descripción

Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/1/enc_flag).
## Pistas

1. Engaging in various decoding processes is of utmost importance

## Solución

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/1/enc_flag`
`--2025-05-12 20:35:32--  https://artifacts.picoctf.net/c_titan/1/enc_flag`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.43, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 73 [application/octet-stream]`
`Saving to: 'enc_flag'`

`enc_flag                          100%[==========================================================>]      73  --.-KB/s    in 0s`      

`2025-05-12 20:35:33 (31.5 MB/s) - 'enc_flag' saved [73/73]`

`OmarSC-picoctf@webshell:~$ ls`
`enc_flag`
`Sebas115-picoctf@webshell:~/crypto/interencdec$ cat enc_flag` 
`YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyeG9OakJzTURCcGZRPT0nCg==`

`OmarSC-picoctf@webshell:~$echo 'YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyeG9OakJzTURCcGZRPT0nCg==' | base64 -d`
`b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ=='`

`OmarSC-picoctf@webshell:~$ echo 'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ==' | base64 -d`
`wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}`

`ROT13` 

`picoCTF{caesar_d3cr9pt3d_ea60e00b}`


## Notas Adicionales



## Referencias
- 

