## Descripción

Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/89b371a46702a31aa9931a2a2b12f8bf/pico_img.png).
## Pistas

1. What does meta mean in the context of files?
2. Ever heard of metadata?

## Solución

`OmarSC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/89b371a46702a31aa9931a2a2b12f8bf/pico_img.png`
`--2025-04-01 18:27:06--  https://jupiter.challenges.picoctf.org/static/89b371a46702a31aa9931a2a2b12f8bf/pico_img.png`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 108795 (106K) [application/octet-stream]`
`Saving to: 'pico_img.png'`

`pico_img.png                              100%[===================================================================================>] 106.25K  --.-KB/s    in 0.05s`   

`2025-04-01 18:27:06 (2.17 MB/s) - 'pico_img.png' saved [108795/108795]`

`OmarSC-picoctf@webshell:~$ strigns -n20 pico_img.png` 
`-bash: strigns: command not found`
`OmarSC-picoctf@webshell:~$ strings -n20 pico_img.png` 
`"iTXtXML:com.adobe.xmp`
`" id="W5M0MpCehiHzreSzNTczkc9d"?> <x:xmpmeta xmlns:x="adobe:ns:meta/" x:xmptk="Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27        "> <rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"> <rdf:Description rdf:about="" xmlns:xmp="http://ns.adobe.com/xap/1.0/" xmlns:xmpMM="http://ns.adobe.com/xap/1.0/mm/" xmlns:stRef="http://ns.adobe.com/xap/1.0/sType/ResourceRef#" xmp:CreatorTool="Adobe Photoshop CS6 (Windows)" xmpMM:InstanceID="xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B" xmpMM:DocumentID="xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B"> <xmpMM:DerivedFrom stRef:instanceID="xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B" stRef:documentID="xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B"/> </rdf:Description> </rdf:RDF> </x:xmpmeta> <?xpacket end="r"?>`
`picoCTF{s0_m3ta_eb36bf44}`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales



## Referencias
- 


