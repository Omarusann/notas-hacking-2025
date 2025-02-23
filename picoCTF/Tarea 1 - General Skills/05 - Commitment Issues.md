## Descripción

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/76/challenge.zip)
## Pistas

1. Version control can help you recover files if you change or lose them!
2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
3. You can 'checkout' commits to see the files inside them

## Solución

`OmarSC-picoctf@webshell:~$ ls`
`challenge.zip  drop-in`
`OmarSC-picoctf@webshell:~$ cd drop-in/`
`OmarSC-picoctf@webshell:~/drop-in$ ls`
`message.txt`
`OmarSC-picoctf@webshell:~/drop-in$ git reflog`
`a6dca68 (HEAD -> master) HEAD@{0}: commit: remove sensitive info`
`e720dc2 HEAD@{1}: commit (initial): create flag`
`OmarSC-picoctf@webshell:~/drop-in$ git checkout e720dc2`
`Note: switching to 'e720dc2'.`

`You are in 'detached HEAD' state. You can look around, make experimental`
`changes and commit them, and you can discard any commits you make in this`
`state without impacting any branches by switching back to a branch.`

`If you want to create a new branch to retain commits you create, you may`
`do so (now or later) by using -c with the switch command. Example:`

  `git switch -c <new-branch-name>`

`Or undo this operation with:`

  `git switch -`

`Turn off this advice by setting config variable advice.detachedHead to false`

`HEAD is now at e720dc2 create flag`
`OmarSC-picoctf@webshell:~/drop-in$ git checkout a6dca68`
`Previous HEAD position was e720dc2 create flag`
`HEAD is now at a6dca68 remove sensitive info`
`OmarSC-picoctf@webshell:~/drop-in$ ls`
`message.txt`
`OmarSC-picoctf@webshell:~/drop-in$ cat message.txt` 
`TOP SECRET`
`OmarSC-picoctf@webshell:~/drop-in$ git checkout e720dc2`
`Previous HEAD position was a6dca68 remove sensitive info`
`HEAD is now at e720dc2 create flag`
`OmarSC-picoctf@webshell:~/drop-in$ cat message.txt` 
`picoCTF{s@n1t1z3_7246792d}`
`OmarSC-picoctf@webshell:~/drop-in$`


## Notas Adicionales

Con el `"reflog"` se pueden ver  los cambios registrados en las confirmaciones y ramas de un repositorio Git. Para después usar un `"checkout"` con el número que nos arrojo ese confirmación.

## Referencias
- 

