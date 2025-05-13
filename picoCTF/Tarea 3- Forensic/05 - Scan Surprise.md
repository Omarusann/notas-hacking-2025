## Descripción

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/16/challenge.zip)

Additional details will be available after launching your challenge instance.

The same files are accessible via SSH here:`ssh -p 50625 ctf-player@atlas.picoctf.net`Using the password `6abf4a82`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Pistas

1. QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
2. Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
3. If you don't have access to a phone, you can also use zbar-tools to convert an image to text

## Solución




## Notas Adicionales
`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/ScanSurprise]`
`└─$ wget https://artifacts.picoctf.net/c_atlas/16/challenge.zip`
`--2025-05-13 03:07:15--  https://artifacts.picoctf.net/c_atlas/16/challenge.zip`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.61, 3.161.55.100, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 736 [application/octet-stream]`
`Saving to: ‘challenge.zip’`

`challenge.zip                    100%[==========================================================>]     736  --.-KB/s    in 0.001s`  

`2025-05-13 03:07:16 (776 KB/s) - ‘challenge.zip’ saved [736/736]`


`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/ScanSurprise]`
`└─$ unzip challenge.zip` 
`Archive:  challenge.zip`
   `creating: home/ctf-player/drop-in/`
 `extracting: home/ctf-player/drop-in/flag.png`  

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/ScanSurprise]`
`└─$ cd home`        

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/ScanSurprise/home]`
`└─$ ls`
`ctf-player`

`┌──(kali㉿kali)-[~/Desktop/tarea3Forensic/ScanSurprise/home]`
`└─$ cd ctf-player/drop-in` 

`┌──(kali㉿kali)-[~/…/ScanSurprise/home/ctf-player/drop-in]`
`└─$ ls`
`flag.png`

`┌──(kali㉿kali)-[~/…/ScanSurprise/home/ctf-player/drop-in]`
`└─$ cat flag.png`         
`�PNG`
`▒`
`IHDRcc��,�PLTE�����tRNS��ȵ��    pHYs`

                                    `��~��IDAT8���1�` 
`��ɮg���� �8���u=��AzsVv)�gfaδ�����<;x�ER>���p����Љ�PG��@�5ظ\ 4H�Ėk q��e@r��4]�Q��Ly��  ���?��!D`
                                                    `�N▒N�DqG�j�I�▒�\8��,+�-�l��S�פ�^YI���ȉN���޳�h�v͵DN۾4��ry��Ҳ��7�9⑶ ��%P��z���+���JI��}�⽲�`
`�IEND�B�`                                                                                                                                    
`┌──(kali㉿kali)-[~/…/ScanSurprise/home/ctf-player/drop-in]`
`└─$` 


`picoCTF{p33k_@_b00_7843f77c}`
## Referencias
- 

