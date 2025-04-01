## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Pistas

1. Try using a tool like Wireshark
2. What are streams?

## Solución

`OmarSC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap`
`--2025-04-01 18:35:34--  https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 239455 (234K) [application/octet-stream]`
`Saving to: 'capture.pcap'`

`capture.pcap        100%[==================>] 233.84K  --.-KB/s    in 0.1s`    

`2025-04-01 18:35:35 (1.96 MB/s) - 'capture.pcap' saved [239455/239455]`

`OmarSC-picoctf@webshell:~$ wireshark capture.pcap &`


`Luego buscamos UDP, le damos click derecho en "Fllow" y luego en UDP Stream`

`Cambiamos lo de stream de 4 a 6 y ya estaria` 

![[Pasted image 20250401125508.png]]

`picoCTF{StaT31355_636f6e6e}`
## Notas Adicionales



## Referencias
- 

