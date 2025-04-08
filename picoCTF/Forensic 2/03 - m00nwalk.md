## Descripción

Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.
## Pistas

1. How did pictures from the moon landing get sent back to Earth?
2. What is the CMU mascot?, that might help select a RX option

## Solución

`──(kali㉿kali)-[~]`
`└─$ wget https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav`
`--2025-04-08 14:31:32--  https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav`
`Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8`
`Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.`
`HTTP request sent, awaiting response... 200 OK`
`Length: 11066998 (11M) [application/octet-stream]`
`Saving to: ‘message.wav’`

`message.wav                100%[========================================>]  10.55M  4.81MB/s    in 2.2s`    

`2025-04-08 14:31:35 (4.81 MB/s) - ‘message.wav’ saved [11066998/11066998]`

                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ sstv`                        
`usage: sstv [-h] [-d AUDIO_FILE] [-o OUTPUT_FILE] [-s SKIP] [-V] [--list-modes] [--list-audio-formats]`
            `[--list-image-formats]`

`options:`
  `-h, --help            show this help message and exit`
  `-d AUDIO_FILE, --decode AUDIO_FILE`
                        `decode SSTV audio file`
  `-o OUTPUT_FILE, --output OUTPUT_FILE`
                        `save output image to custom location`
  `-s SKIP, --skip SKIP  time in seconds to start decoding signal at`
  `-V, --version         show program's version number and exit`
  `--list-modes          list supported SSTV modes`
  `--list-audio-formats  list supported audio file formats`
  `--list-image-formats  list supported image file formats`

`examples:`
  `Decode local SSTV audio file named 'audio.ogg' to 'result.png':`
    `$ sstv -d audio.ogg`

  `Decode SSTV audio file in /tmp to './image.jpg':`
    `$ sstv -d /tmp/signal.wav -o ./image.jpg`

  `Start decoding SSTV signal at 50.5 seconds into the audio`
    `$ sstv -d audio.ogg -s 50.50`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ sstv -d message.wav -o flag.png`
`[sstv] Searching for calibration header... Found!`    
`[sstv] Detected SSTV mode Scottie 1`
`[sstv] Decoding image...   [##########################################################################] 100%`
`[sstv] Drawing image data...`
`[sstv] ...Done!`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$ open flag.png`
                                                                                                            
`┌──(kali㉿kali)-[~]`
`└─$` 


![[Pasted image 20250408123449.png]]

picoCTF{beep_boop_im_in_space}
## Notas Adicionales



## Referencias
- 

