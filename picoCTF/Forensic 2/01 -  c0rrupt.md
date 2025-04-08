## Descripción

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Pistas

1. Try fixing the file header

## Solución

`┌──(kali㉿kali)-[~]`
`┌──(kali㉿kali)-[~]`
`└─$ wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery`       
`--2025-04-08 14:51:10--  https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 202940 (198K) [application/octet-stream]`
`Saving to: ‘mystery’`

`mystery                    100%[========================================>] 198.18K  1.24MB/s    in 0.2s`    

`2025-04-08 14:51:11 (1.24 MB/s) - ‘mystery’ saved [202940/202940]`

                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ xxd -l 100 mystery`       
`00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR`
`00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..`
`00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......`
`00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...`
`00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I`
`00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?`
`00000060: 8e64 cd71                                .d.q`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ cp mystery flag.png`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ cp mystery flag2.png`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ xxd -l 100 flag2.png` 
`00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR`
`00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..`
`00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......`
`00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...`
`00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I`
`00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?`
`00000060: 8e64 cd71                                .d.q`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ xxd -g 9 -l 100 flag2.png` 
`00000000: 89654e340d0ab0aa00 00000d43224452  .eN4........C"DR`
`00000010: 0000066a0000044708 020000007c8bab  ...j...G.....|..`
`00000020: 780000000173524742 00aece1ce90000  x....sRGB.......`
`00000030: 000467414d410000b1 8f0bfc61050000  ..gAMA......a...`
`00000040: 000970485973aa0016 25000016250149  ..pHYs...%...%.I`
`00000050: 5224f0aaaaffa5ab44 4554785eecbd3f  R$......DETx^..?`
`00000060: 8e64cd71                           .d.q`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ xxd -g 8 -l 100 flag2.png`
`00000000: 89654e340d0ab0aa 0000000d43224452  .eN4........C"DR`
`00000010: 0000066a00000447 08020000007c8bab  ...j...G.....|..`
`00000020: 7800000001735247 4200aece1ce90000  x....sRGB.......`
`00000030: 000467414d410000 b18f0bfc61050000  ..gAMA......a...`
`00000040: 000970485973aa00 1625000016250149  ..pHYs...%...%.I`
`00000050: 5224f0aaaaffa5ab 444554785eecbd3f  R$......DETx^..?`
`00000060: 8e64cd71                           .d.q`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ hexeditor flag2.png`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ exiftool flag2.png` 
`ExifTool Version Number         : 13.00`
`File Name                       : flag2.png`
`Directory                       : .`
`File Size                       : 203 kB`
`File Modification Date/Time     : 2025:04:08 14:55:18-04:00`
`File Access Date/Time           : 2025:04:08 14:55:18-04:00`
`File Inode Change Date/Time     : 2025:04:08 14:55:18-04:00`
`File Permissions                : -rw-rw-r--`
`File Type                       : PNG`
`File Type Extension             : png`
`MIME Type                       : image/png`
`Warning                         : PNG image did not start with IHDR`
`SRGB Rendering                  : Perceptual`
`Gamma                           : 2.2`
`Pixels Per Unit X               : 2852132389`
`Pixels Per Unit Y               : 5669`
`Pixel Units                     : meters`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ >....`                                                                                                   
`00000060: 8e64cd71                           .d.q`
 

`┌──(kali㉿kali)-[~]`    
`└─$ hexeditor flag2.png`
 

`┌──(kali㉿kali)-[~]`    
`└─$ exiftool flag2.png`                 
`ExifTool Version Number         : 13.00`    
`File Name                       : flag2.png`
`Directory                       : .`     
`File Size                       : 203 kB`                   
`File Modification Date/Time     : 2025:04:08 14:55:18-04:00`
`File Access Date/Time           : 2025:04:08 14:55:18-04:00`
`File Inode Change Date/Time     : 2025:04:08 14:55:18-04:00`
`File Permissions                : -rw-rw-r--`
`File Type                       : PNG`
`File Type Extension             : png`      
`MIME Type                       : image/png`                        
`Warning                         : PNG image did not start with IHDR`
`SRGB Rendering                  : Perceptual`
`Gamma                           : 2.2`       
`Pixels Per Unit X               : 2852132389`
`Pixels Per Unit Y               : 5669`  
`Pixel Units                     : meters`
 
`Y tenemos que restaurar la imagen manualmente` 

`┌──(kali㉿kali)-[~]`
`└─$`

`picoCTF{c0rrupt10n_1847995}`


## Notas Adicionales



## Referencias
- 

