## Descripción

Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.

## Pistas

1. ASCII is one of the most common encodings used in programming
2. We know that the glitch output is valid Python, somehow!
3. Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Solución

`OmarSC-picoctf@webshell:~$ nc saturn.picoctf.net 52352`
`'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'`
`^C`
`OmarSC-picoctf@webshell:~$ python`
`Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux`
`Type "help", "copyright", "credits" or "license" for more information.`
>>> `'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'`
`'picoCTF{gl17ch_m3_n07_a4392d2e}'`



## Notas Adicionales

1. Corrimos el server que nos dieron 
2. luego nos salimos
3. copiamos el ASCII en python (lit todo asi como venia)
4. nos tiro la flag, ya que lo codifico

## Referencias
- 


