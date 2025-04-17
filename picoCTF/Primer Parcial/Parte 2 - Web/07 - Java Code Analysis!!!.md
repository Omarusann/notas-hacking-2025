## Descripción

BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/481/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:58790/).
## Pistas

1. Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2. The 'role' and 'userId' fields in the JWT can be of interest to you!
3. The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4. Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.

## Solución

`El decode del jwt no me deja cambiar el token, sale que es "Invalid Signature"`

`eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiRnJlZSIsImlzcyI6ImJvb2tzaGVsZiIsImV4cCI6MTc0NTUzMzA3MiwiaWF0IjoxNzQ0OTI4MjcyLCJ1c2VySWQiOjEsImVtYWlsIjoidXNlciJ9.q5sLsaaPvnxZVw9Rxt6ao4iRU_yz98Gpu73GFBnXGCg`

`se supone que tenia que cambiar a esto`
`{"role":"Admin","iss":"bookshelf","exp":1745374826,"iat":1744770026,"userId":2,"email":"admin"}`


`dar refresh y ya, pero no me deja el decode jwt`

## Notas Adicionales



## Referencias
- 

