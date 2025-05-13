## Descripción

A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message

Try it [here](http://standard-pizzas.picoctf.net:62609/)!

Additional details will be available after launching your challenge instance.
## Pistas

1. In the country that doesn't exist, the flag persists

## Solución

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/flagsAreStepic]`
`└─$ wget http://standard-pizzas.picoctf.net:62609/flags/upz.png`     
`--2025-05-13 03:27:38--  http://standard-pizzas.picoctf.net:62609/flags/upz.png`
`Resolving standard-pizzas.picoctf.net (standard-pizzas.picoctf.net)... 3.22.195.189`
`Connecting to standard-pizzas.picoctf.net (standard-pizzas.picoctf.net)|3.22.195.189|:62609... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 1788398 (1.7M) [image/png]`
`Saving to: ‘upz.png’`

`upz.png                          100%[==========================================================>]   1.71M  2.83MB/s    in 0.6s`    

`2025-05-13 03:27:39 (2.83 MB/s) - ‘upz.png’ saved [1788398/1788398]`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/flagsAreStepic]`
`└─$ exiftool upz.png`                                                                 
`ExifTool Version Number         : 13.00`
`File Name                       : upz.png`
`Directory                       : .`
`File Size                       : 1788 kB`
`File Modification Date/Time     : 2025:03:05 22:59:01-05:00`
`File Access Date/Time           : 2025:05:13 03:27:39-04:00`
`File Inode Change Date/Time     : 2025:05:13 03:27:39-04:00`
`File Permissions                : -rw-rw-r--`
`File Type                       : PNG`
`File Type Extension             : png`
`MIME Type                       : image/png`
`Image Width                     : 14173`
`Image Height                    : 10630`
`Bit Depth                       : 8`
`Color Type                      : RGB with Alpha`
`Compression                     : Deflate/Inflate`
`Filter                          : Adaptive`
`Interlace                       : Noninterlaced`
`Image Size                      : 14173x10630`
`Megapixels                      : 150.7`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/flagsAreStepic]`
`└─$ stepic -i upz.png -d`
`Command 'stepic' not found, but can be installed with:`
`sudo apt install stepic`
`Do you want to install it? (N/y)y`
`sudo apt install stepic`
`[sudo] password for kali:` 
`Installing:`                     
  `stepic`

`Summary:`
  `Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 1640`
  `Download size: 10.1 kB`
  `Space needed: 50.2 kB / 61.6 GB available`

`Get:1 http://kali.download/kali kali-rolling/main amd64 stepic all 0.5.0-2 [10.1 kB]`
`Fetched 10.1 kB in 1s (15.9 kB/s)`  
`Selecting previously unselected package stepic.`
`(Reading database ... 404869 files and directories currently installed.)`
`Preparing to unpack .../stepic_0.5.0-2_all.deb ...`
`Unpacking stepic (0.5.0-2) ...`
`Setting up stepic (0.5.0-2) ...`
`Processing triggers for doc-base (0.11.2) ...`
`Processing 41 changed doc-base files, 1 added doc-base file...`
`Processing triggers for man-db (2.13.0-1) ...`
`Processing triggers for kali-menu (2024.4.0) ...`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/flagsAreStepic]`
`└─$ stepic -i upz.png -d`
`/usr/lib/python3/dist-packages/PIL/Image.py:3368: DecompressionBombWarning: Image size (150658990 pixels) exceeds limit of 89478485 pixels, could be decompression bomb DOS attack.`
  `warnings.warn(`
`picoCTF{fl4g_h45_fl4g1a2a9157}`                                                                                                                                    
`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/flagsAreStepic]`
`└─$` 



## Notas Adicionales



## Referencias
- 

