## Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/4/challenge.zip)

Additional details will be available after launching your challenge instance.
`ssh -p 52892 ctf-player@atlas.picoctf.net`Using the password `83dcefb7`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

## Pistas

1. Have you ever played hot or cold? Binary search is a bit like that.
2. You have a very limited number of guesses. Try larger jumps between numbers!
3. The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

## Solución

`OmarSC-picoctf@webshell:~$ ssh -p 52892 ctf-player@atlas.picoctf.net`
`ctf-player@atlas.picoctf.net's password:` 
`Welcome to the Binary Search Game!`
`I'm thinking of a number between 1 and 1000.`
`Enter your guess: 456`
`Lower! Try again.`
`Enter your guess: 250`
`Higher! Try again.`
`Enter your guess: 358`
`Lower! Try again.`
`Enter your guess: 320`
`Lower! Try again.`
`Enter your guess: 298`
`Higher! Try again.`
`Enter your guess: 314`
`Lower! Try again.`
`Enter your guess: 306`
`Higher! Try again.`
`Enter your guess: 310`
`Lower! Try again.`
`Enter your guess: 307`
`Higher! Try again.`
`Enter your guess: 308`
`Congratulations! You guessed the correct number: 308`
`Here's your flag: picoCTF{g00d_gu355_ee8225d0}`
`Connection to atlas.picoctf.net closed.`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales

El chiste esta en adivinar exactamente el número, es quizá algo de suerte, ya que al tener solo 10 intentos, no hay tanto margen de error

## Referencias
- 

