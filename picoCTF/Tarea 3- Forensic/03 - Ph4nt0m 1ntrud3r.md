## Descripción

A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.
## Pistas

1. Filter your packets to narrow down your search.
2. Attacks were done in timely manner.
3. Time is essential

## Solución

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/Ph4nt0m1ntrud3r]`
`└─$ wget https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap`
`--2025-05-13 03:01:48--  https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap`
`Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 65.9.149.85, 65.9.149.59, 65.9.149.95, ...`
`Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|65.9.149.85|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 1452 (1.4K) [application/octet-stream]`
`Saving to: ‘myNetworkTraffic.pcap’`

`myNetworkTraffic.pcap            100%[==========================================================>]   1.42K  --.-KB/s    in 0s`      

`2025-05-13 03:01:49 (44.3 MB/s) - ‘myNetworkTraffic.pcap’ saved [1452/1452]`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/Ph4nt0m1ntrud3r]`
`└─$ exiftool myNetworkTraffic.pcap` 
`ExifTool Version Number         : 13.00`
`File Name                       : myNetworkTraffic.pcap`
`Directory                       : .`
`File Size                       : 1452 bytes`
`File Modification Date/Time     : 2025:03:05 22:31:41-05:00`
`File Access Date/Time           : 2025:05:13 03:01:49-04:00`
`File Inode Change Date/Time     : 2025:05:13 03:01:49-04:00`
`File Permissions                : -rw-rw-r--`
`Error                           : Unknown file type`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/Ph4nt0m1ntrud3r]`
`└─$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4 | awk '{print $6}' | xxd -p -r | base64 -d`
`Warning: program compiled against libxml 212 using older 209`
`picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}`                                                                                                                                    
`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/Ph4nt0m1ntrud3r]`
`└─$` 



## Notas Adicionales



## Referencias
- 

