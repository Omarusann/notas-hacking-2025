## Descripción

Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:64302/), and find the flag!
## Pistas

1. A bookmarklet is a bookmark that runs JavaScript instead of loading a webpage.
2. What happens when you click a bookmarklet?
3. Web browsers have other ways to run JavaScript too.

## Solución

`Copiamos el codigo y lo ejecutamos en la consola`

        `javascript:(function() {`
            `var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÓÇ¡¥Ìí";`
            `var key = "picoctf";`
            `var decryptedFlag = "";`
            `for (var i = 0; i < encryptedFlag.length; i++) {`
                `decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);`
            `}`
            `alert(decryptedFlag);`
        `})();`


`picoCTF{p@g3_turn3r_0c0d211f}`

## Notas Adicionales



## Referencias
- 

