## Descripción
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)

## Pistas
1. Are equality and assignment the same symbol?
2. To view the file in the webshell, do: `$ nano fixme2.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

`OmarSC-picoctf@webshell:~$ ls`
`README.txt  fixme2.py`
`OmarSC-picoctf@webshell:~$ nano fixme2.py`
`OmarSC-picoctf@webshell:~$ python3 fixme2.py`
`That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales

El problema del código estaba en la comparación que se le estaba haciendo, ya que estaba `"="` en lugar de `"=="` 

## Referencias
- 
