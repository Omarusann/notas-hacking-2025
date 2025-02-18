## Descripción

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)
## Pistas

Can grep be instructed to look at every file in a directory and its subdirectories?

## Solución

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/504/big-zip-files.zip`
`unzip big-zip-files.zip`
grep -R picoCTF{
`picoCTF{gr3p_15_m4g1c_ef8790dc}`

## Notas Adicionales

- Se tuvieron que descomprimir todos los archivos para poder buscarlos
- grep -R picoCTF{ - se uso ese comando para que se buscara en todos los archivos la cadena que dijera pico

## Referencias
- 

