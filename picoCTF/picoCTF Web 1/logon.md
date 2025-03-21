## Descripción

The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or http://jupiter.challenges.picoctf.org:44573
## Pistas

1. Hmm it doesn't seem to check anyone's password, except for Joe's?

## Solución

`Inspeccionamos la parte del network a la hora de solicitar el login`
![[Pasted image 20250320122353.png]]

`Observamos los headers` 

![[Pasted image 20250320122517.png]]

`Ponemos el modo RAW`
![[Pasted image 20250320122745.png]]

`Descargamos el editor de cookies y modificamos el apartado de False a True`
![[Pasted image 20250320123930.png]]


![[Pasted image 20250320124031.png]]

`picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}`
## Notas Adicionales



## Referencias
- 

