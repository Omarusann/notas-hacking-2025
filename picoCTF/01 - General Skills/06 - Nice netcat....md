## Descripción

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22902`, but it doesn't speak English...

## Pistas

1. You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)
2. You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)

## Solución

`OmarSC-picoctf@webshell:~$ nc mercury.picoctf.net 22902`
`112` 
`105` 
`99` 
`111` 
`67` 
`84` 
`70` 
`123` 
`103` 
`48` 
`48` 
`100` 
`95` 
`107` 
`49` 
`116` 
`116` 
`121` 
`33` 
`95` 
`110` 
`49` 
`99` 
`51` 
`95` 
`107` 
`49` 
`116` 
`116` 
`121` 
`33` 
`95` 
`100` 
`51` 
`100` 
`102` 
`100` 
`54` 
`100` 
`102` 
`125` 
`10` 
`^C`
`OmarSC-picoctf@webshell:~$ nc mercury.picoctf.net 22902 > hola`
`^C`
`OmarSC-picoctf@webshell:~$ python`
`Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux`
`Type "help", "copyright", "credits" or "license" for more information.`
>>> `todo = open('hola')`
>>> `todo`
`<_io.TextIOWrapper name='hola' mode='r' encoding='UTF-8'>`
>>> 

`picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}`
## Notas Adicionales



## Referencias
- 

