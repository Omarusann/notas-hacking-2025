## Descripción

Help us test the form by submiting the username as `test` and password as `test!`The website running [here](http://saturn.picoctf.net:49596/).
## Pistas

1. any redirections?

## Solución

1. `Ingresamos a la página y pondremos las siguientes claves`
	- `User: test`
	- `Password: test!`
2. `Pasa por 2 procesos para avanzar`
3. `Retrocedemos y copiamos los id que nos arroja`

`http://saturn.picoctf.net:49596/next-page/id=bF90aGVfd2F5XzNkOWUzNjk3fQ==`

`bF90aGVfd2F5XzNkOWUzNjk3fQ== = l_the_way_3d9e3697}`

`http://saturn.picoctf.net:49596/next-page/id=cGljb0NURntwcm94aWVzX2Fs`

`cGljb0NURntwcm94aWVzX2Fs = picoCTF{proxies_al`

`picoCTF{proxies_all_the_way_3d9e3697}`
## Notas Adicionales



## Referencias
- 

