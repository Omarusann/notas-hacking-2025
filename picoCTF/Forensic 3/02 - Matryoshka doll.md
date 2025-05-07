## Descripción

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg)
## Pistas

1. Wait, you can hide files inside files? But how do you find them?
2. Make sure to submit the flag as picoCTF{XXXXX}

## Solución

`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska]`
`└─$ wget https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg`              
`--2025-05-06 14:41:33--  https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 651635 (636K) [application/octet-stream]`
`Saving to: ‘dolls.jpg’`

`dolls.jpg                                                  100%[========================================================================================================================================>] 636.36K   268KB/s    in 2.4s`    

`2025-05-06 14:41:40 (268 KB/s) - ‘dolls.jpg’ saved [651635/651635]`


`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska]`
`└─$ file dolls.jpg`                                           
`dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced`

`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska]`
`└─$ eog dolls.jpg` 

`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska]`
`└─$ binwalk dolls.jpg`   

`DECIMAL       HEXADECIMAL     DESCRIPTION`
--------------------------------------------------------------------------------
`0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced`
`3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8`
`272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378955, uncompressed size: 383936, name: base_images/2_c.jpg`
`651613        0x9F15D         End of Zip archive, footer length: 22`


`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska]`
`└─$ unzip dolls.jpg` 
`Archive:  dolls.jpg`
`warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile`
  `(attempting to process anyway)`
  `inflating: base_images/2_c.jpg`     

`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska]`
`└─$ cd base_images` 

`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska/base_images]`
`└─$ unzip 2_c.jpg`  
`Archive:  2_c.jpg`
`warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile`
  `(attempting to process anyway)`
  `inflating: base_images/3_c.jpg`     

`┌──(kali㉿kali)-[~/Desktop/forensic3/matrioska/base_images]`
`└─$ cd base_images` 

`┌──(kali㉿kali)-[~/…/forensic3/matrioska/base_images/base_images]`
`└─$ ls`
`3_c.jpg`

`┌──(kali㉿kali)-[~/…/forensic3/matrioska/base_images/base_images]`
`└─$ unzip 3_c.jpg` 
`Archive:  3_c.jpg`
`warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile`
  `(attempting to process anyway)`
  `inflating: base_images/4_c.jpg`     

`┌──(kali㉿kali)-[~/…/forensic3/matrioska/base_images/base_images]`
`└─$ ls`
`3_c.jpg  base_images`

`┌──(kali㉿kali)-[~/…/forensic3/matrioska/base_images/base_images]`
`└─$ cd base_images`    

`┌──(kali㉿kali)-[~/…/matrioska/base_images/base_images/base_images]`
`└─$ ls`
`4_c.jpg`

`┌──(kali㉿kali)-[~/…/matrioska/base_images/base_images/base_images]`
`└─$ unzip 4_c.jpg` 
`Archive:  4_c.jpg`
`warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile`
  `(attempting to process anyway)`
  `inflating: flag.txt`                

`┌──(kali㉿kali)-[~/…/matrioska/base_images/base_images/base_images]`
`└─$ cat flag.txt`  
`picoCTF{ac0072c423ee13bfc0b166af72e25b61}`                                                                                                                                                                                                                                            
`┌──(kali㉿kali)-[~/…/matrioska/base_images/base_images/base_images]`
`└─$` 



## Notas Adicionales



## Referencias
- 

