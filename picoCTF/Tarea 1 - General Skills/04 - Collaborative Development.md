## Descripción

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/71/challenge.zip)
## Pistas

1. `git branch -a` will let you see available branches
2. How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
3. Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.

## Solución

`OmarSC-picoctf@webshell:~$ ls`
`challenge.zip  drop-in`
`OmarSC-picoctf@webshell:~$ cd drop-in/`
`OmarSC-picoctf@webshell:~/drop-in$ git branch -a`
`OmarSC-picoctf@webshell:~/drop-in$ git checkout feature/part-1`
`Switched to branch 'feature/part-1'`
`OmarSC-picoctf@webshell:~/drop-in$ ls`
`flag.py`
`OmarSC-picoctf@webshell:~/drop-in$ cat flag.py`
`print("Printing the flag...")`
`print("picoCTF{t3@mw0rk_", end='')OmarSC-picoctf@webshell:~/drop-in$ git checkout feature/part-2`
`Switched to branch 'feature/part-2'`
`OmarSC-picoctf@webshell:~/drop-in$ cat flag.py` 
`print("Printing the flag...")`

`print("m@k3s_th3_dr3@m_", end='')OmarSC-picoctf@webshell:~/drop-in$ git checkout feature/part-3`
`Switched to branch 'feature/part-3'`
`OmarSC-picoctf@webshell:~/drop-in$ cat flag.py` 
`print("Printing the flag...")`

`print("w0rk_4c24302f}")`
`OmarSC-picoctf@webshell:~/drop-in$` 

`picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_4c24302f}`

## Notas Adicionales

Se tenían que unir las respuestas por partes que nos daba cada archivo que estaba en la commit, a través del `"git checkout"`, veíamos que tenía cada commit, y al ejecutarse, nos daban una parte de la bandera.

## Referencias
- 

