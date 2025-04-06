## Descripción

Can you get the flag?Go to this [website](http://saturn.picoctf.net:59853/) and see what you can discover.
## Pistas

1. How is the password checked on this website?

## Solución

`Mandamos el login failed e inspeccionamos el archivo Secure.js`

`function checkPassword(username, password)`
`{`
  `if( username === 'admin' && password === 'strongPassword098765' )`
  `{`
    `return true;`
  `}`
  `else`
  `{`
    `return false;`
  `}`
`}`

`picoCTF{j5_15_7r4n5p4r3n7_05df90c8}`
## Notas Adicionales



## Referencias
- 

