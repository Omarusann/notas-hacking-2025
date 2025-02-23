## Descripción

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/67/challenge.zip)
## Pistas

1. The `cat` command will let you read a file, but that won't help you here!
2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3. When committing a file with git, a message can (and should) be included.

## Solución

`OmarSC-picoctf@webshell:~$ ls`
`challenge.zip  drop-in`
`OmarSC-picoctf@webshell:~$ cd drop-in/`
`OmarSC-picoctf@webshell:~/drop-in$ ls`
`message.txt`
`OmarSC-picoctf@webshell:~/drop-in$ cat message.txt` 
`This is what I was working on, but I'd need to look at my commit history to know why...OmarSC-picoctf@webshell:~/drop-in$ git log`
`OmarSC-picoctf@webshell:~/drop-in$` 
`commit b92bdd8ec87a21ba45e77bd9bed3e4893faafd0f (HEAD -> master)`
`Author: picoCTF <ops@picoctf.com>`
`Date:   Sat Mar 9 21:10:29 2024 +0000`

    `picoCTF{t1m3m@ch1n3_5cde9075}`

## Notas Adicionales

Solo utilizamos el `"git log"` para ver el último commit que se realizo, y que comentario se tenia

## Referencias
- 


