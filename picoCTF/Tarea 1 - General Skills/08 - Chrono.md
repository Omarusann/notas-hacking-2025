## Descripción

How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:
```
Server: saturn.picoctf.net
Port: 53671
Username: picoplayer 
Password: pYkku7iMsS
```
## Pistas

1. (None)

## Solución

`OmarSC-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 53671`
`The authenticity of host '[saturn.picoctf.net]:53671 ([13.59.203.175]:53671)' can't be established.`
`ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.`
`This host key is known by the following other names/addresses:`
    `~/.ssh/known_hosts:9: [hashed name]`
`Are you sure you want to continue connecting (yes/no/[fingerprint])? yes`
`Warning: Permanently added '[saturn.picoctf.net]:53671' (ED25519) to the list of known hosts.`
`picoplayer@saturn.picoctf.net's password:` 
`Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)`

 * `Documentation:  https://help.ubuntu.com`
 * `Management:     https://landscape.canonical.com`
 * `Support:        https://ubuntu.com/advantage`

`This system has been minimized by removing packages and content that are`
`not required on a system that users do not log into.`

`To restore this content, you can run the 'unminimize' command.`

`The programs included with the Ubuntu system are free software;`
`the exact distribution terms for each program are described in the`
`individual files in /usr/share/doc/*/copyright.`

`Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by`
`applicable law.`

`picoplayer@challenge:~$ cat /etc/crontab`
`picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}`
`picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.`
`Connection to saturn.picoctf.net closed.`
`OmarSC-picoctf@webshell:~$` 


## Notas Adicionales

- El archivo `/etc/crontab` es un archivo de Linux que contiene la información sobre los trabajos que se deben ejecutar de manera automática.

## Referencias
- 

