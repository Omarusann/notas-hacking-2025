## Descripción

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090
## Pistas

1. What is that cookie?
2. Have you heard of JWT?

## Solución

1. `Accedemos al sitio`
2. `Ingresamos con nuestro nombre` 
3. `Buscamos la cookie con el "Cookie Editor"`
`eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiT21hciJ9.CtS_cvXvkcmUiFtr7ToUjMX1Xbpueh2ilBu369Qxh5k`
4. `Ingresamos a https://jwt.io/ para modificar la cookie`
5. `Modificamos la cookie cambiandole nuestro nombre por "admin" y cambiando la parte que dice "secret" por "ilovepico"`
![[Pasted image 20250327143726.png]]

6. `Nos arrojará esta nueva cookie`
`eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s`

7. `La pegamos, guardamos y damos refresh`

`picoCTF{jawt_was_just_what_you_thought_f859ab2f}`

## Notas Adicionales

No me dejaba modificar el campo de la cookie en el JWT Debugger

## Referencias
- 

