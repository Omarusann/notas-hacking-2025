## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Pistas

1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?

## Solución

`┌──(kali㉿kali)-[~]`
`└─$ cd /home/kali/Desktop/forensic3/`

`┌──(kali㉿kali)-[~/Desktop/forensic3]`
`└─$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap`
`--2025-05-06 14:16:46--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 13163 (13K) [application/octet-stream]`
`Saving to: ‘capture.pcap’`

`capture.pcap                                               100%[========================================================================================================================================>]  12.85K  --.-KB/s    in 0s`      

`2025-05-06 14:16:54 (237 MB/s) - ‘capture.pcap’ saved [13163/13163]`


`┌──(kali㉿kali)-[~/Desktop/forensic3]`
`└─$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key`
`--2025-05-06 14:17:02--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 1704 (1.7K) [application/octet-stream]`
`Saving to: ‘picopico.key’`

`picopico.key                                               100%[========================================================================================================================================>]   1.66K  --.-KB/s    in 0s`      

`2025-05-06 14:17:11 (30.5 MB/s) - ‘picopico.key’ saved [1704/1704]`


`┌──(kali㉿kali)-[~/Desktop/forensic3]`
`└─$ wireshark capture.pcap &`                                                                        
`[1] 2689`

`┌──(kali㉿kali)-[~/Desktop/forensic3]`
`└─$ Warning: program compiled against libxml 212 using older 209`
`ssldump /r capture.pcap -k picopico.key -d | pico -A 2`
`PCAP: eth0: You don't have permission to perform this capture on that device (socket: Operation not permitted)`
                                                                                                              `ERROR: Aborting`
`Standard input is not a terminal`

`┌──(kali㉿kali)-[~/Desktop/forensic3]`
`└─$ ssldump -r capture.pcap -k picopico.key -d | pico -A 2`
`Standard input is not a terminal`
`^[[B^[[B^[[B^[[B^[[B^[[B^[[B^[[B^[[BShort read: -1295 bytes available (expecting 2)`

`┌──(kali㉿kali)-[~/Desktop/forensic3]`
`└─$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A 2`
`Short read: -1295 bytes available (expecting 2)`
`Short read: -1295 bytes available (expecting 2)`
`Short read: -1295 bytes available (expecting 2)`
    `61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong`
    `73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac`
    `6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L`
--
    `67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs`
    `68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack`
    `65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le`

`┌──(kali㉿kali)-[~/Desktop/forensic3]`
`└─$` 

picoCTF{nongshim.shrimp.crackers}

|
## Notas Adicionales



## Referencias
- 

