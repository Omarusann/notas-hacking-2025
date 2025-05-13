## Descripción

How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/129/unknown.zip).
## Pistas

1. How can you view the information about the picture?
2. If something isn't in the expected form, maybe it deserves attention?

## Solución

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/CanYouSee]`
`└─$ wget https://artifacts.picoctf.net/c_titan/129/unknown.zip`                                  
`--2025-05-13 02:50:17--  https://artifacts.picoctf.net/c_titan/129/unknown.zip`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.61, 3.161.55.26, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 2252200 (2.1M) [application/octet-stream]`
`Saving to: ‘unknown.zip’`

`unknown.zip                      100%[==========================================================>]   2.15M  5.03MB/s    in 0.4s`    

`2025-05-13 02:50:18 (5.03 MB/s) - ‘unknown.zip’ saved [2252200/2252200]`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/CanYouSee]`
`└─$ ls`
`unknown.zip`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/CanYouSee]`
`└─$ unzip unknown.zip` 
`Archive:  unknown.zip`
  `inflating: ukn_reality.jpg`         

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/CanYouSee]`
`└─$ exiftool ukn_reality.jpg` 
`ExifTool Version Number         : 13.00`
`File Name                       : ukn_reality.jpg`
`Directory                       : .`
`File Size                       : 2.3 MB`
`File Modification Date/Time     : 2024:03:11 20:05:53-04:00`
`File Access Date/Time           : 2024:03:11 20:05:53-04:00`
`File Inode Change Date/Time     : 2025:05:13 02:50:39-04:00`
`File Permissions                : -rw-r--r--`
`File Type                       : JPEG`
`File Type Extension             : jpg`
`MIME Type                       : image/jpeg`
`JFIF Version                    : 1.01`
`Resolution Unit                 : inches`
`X Resolution                    : 72`
`Y Resolution                    : 72`
`XMP Toolkit                     : Image::ExifTool 11.88`
`Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==`
`Image Width                     : 4308`
`Image Height                    : 2875`
`Encoding Process                : Baseline DCT, Huffman coding`
`Bits Per Sample                 : 8`
`Color Components                : 3`
`Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)`
`Image Size                      : 4308x2875`
`Megapixels                      : 12.4`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/CanYouSee]`
`└─$` 


`cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg== (base64)`
`picoCTF{ME74D47A_HIDD3N_b32040b8}`

## Notas Adicionales



## Referencias
- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnROUlRjMFJEUTNRVjlJU1VSRU0wNWZZak15TURRd1lqaDlDZz09&ieol=CRLF

