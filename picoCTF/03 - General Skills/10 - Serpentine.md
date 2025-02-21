## Descripción

Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/36/serpentine.py)
## Pistas

1. Try running the script and see what happens
2. In the webshell, try examining the script with a text editor like `nano`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

`OmarSC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/36/serpentine.py`
`--2025-02-21 08:46:47--  https://artifacts.picoctf.net/c/36/serpentine.py`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.18, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 2550 (2.5K) [application/octet-stream]`
`Saving to: 'serpentine.py'`

`serpentine.py                            100%[===============================================================================>]   2.49K  --.-KB/s    in 0s`      

`2025-02-21 08:46:47 (684 MB/s) - 'serpentine.py' saved [2550/2550]`

`OmarSC-picoctf@webshell:~$ nano serpentine.py`
`OmarSC-picoctf@webshell:~$ python3 serpentine.py`

    `Y`
  `.-^-.`
 `/     \      .- ~ ~ -.`
`()     ()    /   _ _   .                     _ _ _`
 `\_   _/    /  /     \   \                . ~  _ _  ~ .`
   `| |     /  /       \   \             .' .~       ~-. .`
   `| |    /  /         )   )           /  /             ..`
   `\ \_ _/  /         /   /           /  /                '`
    `\_ _ _.'         /   /           (  (`
                    `/   /             \  \`
                   `/   /               \  \`
                  `/   /                 )  )`
                 `(   (                 /  /`
                  `.  .             .'  /`
                    `.   ~ - - - - ~   .'`
                       `~ . _ _ _ _ . ~`

`Welcome to the serpentine encourager!`


`a) Print encouragement`
`b) Print flag`
`c) Quit`

`What would you like to do? (a/b/c) b`

`Oops! I must have misplaced the print_flag function! Check my source code!`

`What would you like to do? (a/b/c) c` 
`OmarSC-picoctf@webshell:~$ nano serpentine.py`
`OmarSC-picoctf@webshell:~$ python3 serpentine.py`

    `Y`
  `.-^-.`
 `/     \      .- ~ ~ -.`
`()     ()    /   _ _   .                     _ _ _`
 `\_   _/    /  /     \   \                . ~  _ _  ~ .`
   `| |     /  /       \   \             .' .~       ~-. .`
   `| |    /  /         )   )           /  /             ..`
   `\ \_ _/  /         /   /           /  /                '`
    `\_ _ _.'         /   /           (  (`
                    `/   /             \  \`
                   `/   /               \  \`
                  `/   /                 )  )`
                 `(   (                 /  /`
                  `.  .             .'  /`
                    `.   ~ - - - - ~   .'`
                       `~ . _ _ _ _ . ~`

`Welcome to the serpentine encourager!`


`a) Print encouragement`
`b) Print flag`
`c) Quit`

`What would you like to do? (a/b/c) b`
`picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}`
`a) Print encouragement`
`b) Print flag`
`c) Quit`

`What would you like to do? (a/b/c) c`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales

La solución estaba en modificar el código fuente a través del `"nano"`, para después modificar el print de la opción B  a un `"print_flag()"`

## Referencias
- 