## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Pistas

1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?

## Solución



`┌──(kali㉿kali)-[~/Desktop/forensic3/webnet]`
`└─$ https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key`
`zsh: no such file or directory: https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key`

`┌──(kali㉿kali)-[~/Desktop/forensic3/webnet]`
`└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key`
`--2025-05-06 14:33:38--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 1704 (1.7K) [application/octet-stream]`
`Saving to: ‘picopico.key’`

`picopico.key                                               100%[========================================================================================================================================>]   1.66K  --.-KB/s    in 0s`      

`2025-05-06 14:33:46 (44.0 MB/s) - ‘picopico.key’ saved [1704/1704]`


`┌──(kali㉿kali)-[~/Desktop/forensic3/webnet]`
`└─$ wireshark capture.pcap &`                                                                        
`[2] 10857`

`┌──(kali㉿kali)-[~/Desktop/forensic3/webnet]`
`└─$ Warning: program compiled against libxml 212 using older 209`


`┌──(kali㉿kali)-[~/Desktop/forensic3/webnet]`
`└─$ string vulture.jpg | grep pico`                             
`Command 'string' not found, did you mean:`
  `command 'spring' from deb ruby-spring`
  `command 'strings' from deb binutils`
`Try: sudo apt install <deb name>`

`┌──(kali㉿kali)-[~/Desktop/forensic3/webnet]`
`└─$ strings vulture.jpg | grep pico`

picoCTF{honey.roasted.peanuts}


## Notas Adicionales



## Referencias
- 

