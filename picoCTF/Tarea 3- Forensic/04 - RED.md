## Descripción

RED, RED, RED, REDDownload the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
## Pistas

1. The picture seems pure, but is it though?
2. Red?Ged?Bed?Aed?
3. Check whatever Facebook is called now.

## Solución

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RED]`
`└─$ wget https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png` 
`--2025-05-13 03:04:00--  https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png`
`Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 65.9.149.24, 65.9.149.95, 65.9.149.85, ...`
`Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|65.9.149.24|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 796 [application/octet-stream]`
`Saving to: ‘red.png’`

`red.png                          100%[==========================================================>]     796  --.-KB/s    in 0s`      

`2025-05-13 03:04:00 (19.7 MB/s) - ‘red.png’ saved [796/796]`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RED]`
`└─$ strings red.png`                 
`IHDR`
`tEXtPoem`
`Crimson heart, vibrant and bold,`
`Hearts flutter at your sight.`
`Evenings glow softly red,`
`Cherries burst with sweet life.`
`Kisses linger with your warmth.`
`Love deep as merlot.`
`Scarlet leaves falling softly,`
`Bold in every stroke.x`
`IDATx`
`IEND`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RED]`
`└─$ exiftool red.png`              
`ExifTool Version Number         : 13.00`
`File Name                       : red.png`
`Directory                       : .`
`File Size                       : 796 bytes`
`File Modification Date/Time     : 2025:03:05 22:34:15-05:00`
`File Access Date/Time           : 2025:05:13 03:04:12-04:00`
`File Inode Change Date/Time     : 2025:05:13 03:04:00-04:00`
`File Permissions                : -rw-rw-r--`
`File Type                       : PNG`
`File Type Extension             : png`
`MIME Type                       : image/png`
`Image Width                     : 128`
`Image Height                    : 128`
`Bit Depth                       : 8`
`Color Type                      : RGB with Alpha`
`Compression                     : Deflate/Inflate`
`Filter                          : Adaptive`
`Interlace                       : Noninterlaced`
`Poem                            : Crimson heart, vibrant and bold,.Hearts flutter at your sight..Evenings glow softly red,.Cherries burst with sweet life..Kisses linger with your warmth..Love deep as merlot..Scarlet leaves falling softly,.Bold in every stroke.`
`Image Size                      : 128x128`
`Megapixels                      : 0.016`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RED]`
`└─$ zsteg --lsb --channel rgba red.png` 
`b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="`
`b2,rgba,lsb,xy      .. file: OpenPGP Secret Key`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RED]`
`└─$ echo cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ== | base64 -d`
`picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}`                                                                                                                                    
`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/RED]`
`└─$` 



## Notas Adicionales



## Referencias
- 

