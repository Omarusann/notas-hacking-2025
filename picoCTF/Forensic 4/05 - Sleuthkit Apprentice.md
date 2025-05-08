## Descripción

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)
## Pistas

1. (None)

## Solución

`OmarSC-picoctf@webshell:/tmp$ ls -la`
`total 102400`
`drwxrwxrwt 1 root           root                  30 May  8 14:56 .`
`drwxr-xr-x 1 root           root                  70 May  8 14:55 ..`
`drwx------ 3 root           root                  41 Mar  5 02:13 .wine-0`
`-rw-rw-r-- 1 OmarSC-picoctf OmarSC-picoctf 104857600 Aug  4  2023 disk.img`
`drwxr-xr-x 2 root           root                   6 Mar  5 02:09 hsperfdata_root`
`drwxr-xr-x 3 root           root                  45 Mar  5 02:13 node-compile-cache`
`OmarSC-picoctf@webshell:/tmp$ wget https://artifacts.picoctf.net/c/137/disk.flag.img.gz`
`--2025-05-08 15:02:35--  https://artifacts.picoctf.net/c/137/disk.flag.img.gz`
`Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.92, ...`
`Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 47534568 (45M) [application/octet-stream]`
`Saving to: 'disk.flag.img.gz'`

`disk.flag.img.gz                          100%[===================================================================================>]  45.33M  1.82MB/s    in 25s`     

`2025-05-08 15:03:00 (1.82 MB/s) - 'disk.flag.img.gz' saved [47534568/47534568]`

`OmarSC-picoctf@webshell:/tmp$ gunzip disk.flag.img.gz` 
`OmarSC-picoctf@webshell:/tmp$ ls -la`
`total 409600`
`drwxrwxrwt 1 root           root                  55 May  8 15:03 .`
`drwxr-xr-x 1 root           root                  70 May  8 14:55 ..`
`drwx------ 3 root           root                  41 Mar  5 02:13 .wine-0`
`-rw-rw-r-- 1 OmarSC-picoctf OmarSC-picoctf 314572800 Mar 16  2023 disk.flag.img`
`-rw-rw-r-- 1 OmarSC-picoctf OmarSC-picoctf 104857600 Aug  4  2023 disk.img`
`drwxr-xr-x 2 root           root                   6 Mar  5 02:09 hsperfdata_root`
`drwxr-xr-x 3 root           root                  45 Mar  5 02:13 node-compile-cache`
`OmarSC-picoctf@webshell:/tmp$ mmls disk.flag.img` 
`DOS Partition Table`
`Offset Sector: 0`
`Units are in 512-byte sectors`

      `Slot      Start        End          Length       Description`
`000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)`
`001:  -------   0000000000   0000002047   0000002048   Unallocated`
`002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)`
`003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)`
`004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)`
`OmarSC-picoctf@webshell:/tmp$ fls -o 206848 disk.flag.img` 
`}Cannot determine file system type`
`OmarSC-picoctf@webshell:/tmp$ fls -o 360448 disk.flag.img` 
`d/d 451:        home`
`d/d 11: lost+found`
`d/d 12: boot`
`d/d 1985:       etc`
`d/d 1986:       proc`
`d/d 1987:       dev`
`d/d 1988:       tmp`
`d/d 1989:       lib`
`d/d 1990:       var`
`d/d 3969:       usr`
`d/d 3970:       bin`
`d/d 1991:       sbin`
`d/d 1992:       media`
`d/d 1993:       mnt`
`d/d 1994:       opt`
`d/d 1995:       root`
`d/d 1996:       run`
`d/d 1997:       srv`
`d/d 1998:       sys`
`d/d 2358:       swap`
`V/V 31745:      $OrphanFiles`
`OmarSC-picoctf@webshell:/tmp$ fls -o 360448 disk.flag.img 451`
`OmarSC-picoctf@webshell:/tmp$ fls -o 360448 disk.flag.img 1995`
`r/r 2363:       .ash_history`
`d/d 3981:       my_folder`
`OmarSC-picoctf@webshell:/tmp$ fls -o 360448 disk.flag.img 2363`
`Error extracting file from image (ext2fs_dir_open_meta: Error reading directory contents: 2363`
`)`
`OmarSC-picoctf@webshell:/tmp$ fls -o 360448 disk.flag.img 23633981`
`Invalid walk range (ext2fs_dir_open_meta: inode value: 23633981`
`)`
`OmarSC-picoctf@webshell:/tmp$ fls -o 360448 disk.flag.img 3981`    
`r/r * 2082(realloc):    flag.txt`
`r/r 2371:       flag.uni.txt`
`OmarSC-picoctf@webshell:/tmp$ icat  -o 360448 disk.flag.img 3981`

`..flag.txtC`
                `flag.uni.txt`
                            `qUOmarSC-picoctf@webshell:/tmp$ icat  -o 360448 disk.flag.img 2371`
`picoCTF{by73_5urf3r_adac6cb4}`
`OmarSC-picoctf@webshell:/tmp$` 


## Notas Adicionales



## Referencias
- 

