## Descripción

🥛
## Pistas

1. Look at the problem category

## Solución

`┌──(kali㉿kali)-[~/Desktop/forensic4/milkslap]`
`└─$ curl -i http://mercury.picoctf.net:58537`
`HTTP/1.1 200 OK`
`Content-type: text/html; charset=UTF-8`

`<!doctype html>`

`<html lang="en">`
`<head>`
  `<meta charset="UTF-8" />`
  `<meta name="viewport" content="width=400" />`
  `<title>🥛</title>`
  `<link rel="stylesheet" href="style.css" />`

`</head>`
`<body>`
  `<div id="image" class="center"></div>`
  `<div id="foot" class="center">`
    `<h1>MilkSlap!</h1>`
    `Inspired by <a href="http://eelslap.com">http://eelslap.com</a> <br>`
    `Credit to: <a href="https://github.com/boxmein">boxmein</a> for code inspiration.`
  `</div>`
  `<script src="script.js">`


`</script>`
`</body>`
`</html>`

`┌──(kali㉿kali)-[~/Desktop/forensic4/milkslap]`
`└─$ wget http://mercury.picoctf.net:58537/concat_v.png`                                              
`--2025-05-08 12:42:32--  http://mercury.picoctf.net:58537/concat_v.png`
`Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142`
`Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:58537... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 18095920 (17M) [image/png]`
`Saving to: ‘concat_v.png’`

`concat_v.png                     100%[==========================================================>]  17.26M  2.91MB/s    in 8.3s`    

`2025-05-08 12:42:48 (2.07 MB/s) - ‘concat_v.png’ saved [18095920/18095920]`


`┌──(kali㉿kali)-[~/Desktop/forensic4/milkslap]`
`└─$ zsteg concat_v.png` 

`imagedata .. text: "\n\n\n\n\n\n\t\t" b1,b,lsb,xy .. text: "picoCTF{imag3_m4n1pul4t10n_sl4p5}\n" <-- b1,bgr,lsb,xy .. <wbStego size=9706075, data="\xB6\xAD\xB6}\xDB\xB2lR\x7F\xDF\x86\xB7c\xFC\xFF\xBF\x02Zr\x8E\xE2Z\x12\xD8q\xE5&MJ-X:\xB5\xBF\xF7\x7F\xDB\xDFI\bm\xDB\xDB\x80m\x00\x00\x00\xB6m\xDB\xDB\xB6\x00\x00\x00\xB6\xB6\x00m\xDB\x12\x12m\xDB\xDB\x00\x00\x00\x00\x00\xB6m\xDB\x00\xB6\x00\x00\x00\xDB\xB6mm\xDB\xB6\xB6\x00\x00\x00\x00\x00m\xDB", even=true, mix=true, controlbyte="["> b2,r,lsb,xy .. file: SoftQuad DESC or font file binary b2,r,msb,xy .. file: VISX image file b2,g,lsb,xy .. file: VISX image file b2,g,msb,xy .. file: SoftQuad DESC or font file binary - version 15722 b2,b,msb,xy .. text: "UfUUUU@UUU" b4,r,lsb,xy .. text: "\"\"\"\"\"#4D" b4,r,msb,xy .. text: "wwww3333" b4,g,lsb,xy .. text: "wewwwwvUS" b4,g,msb,xy .. text: "\"\"\"\"DDDD" b4,b,lsb,xy .. text: "vdUeVwweDFw" b4,b,msb,xy .. text: "UUYYUUUUUUUU"`

`┌──(kali㉿kali)-[~/Desktop/forensic4/milkslap]`
`└─$` 

picoCTF{imag3_m4n1pul4t10n_sl4p5}

## Notas Adicionales



## Referencias
- 

