## Descripción

Dear Threat Intelligence Analyst,Quick heads up - we stumbled upon a shady executable file on one of our employee's Windows PCs. Good news: the employee didn't take the bait and flagged it to our InfoSec crew.Seems like this file sneaked past our Intrusion Detection Systems, indicating a fresh threat with no matching signatures in our database.Can you dive into this file and whip up some YARA rules? We need to make sure we catch this thing if it pops up again.Thanks a bunch!The suspicious file can be downloaded [here](https://challenge-files.picoctf.net/c_standard_pizzas/873ba2368a8d4670859d8fa3110d214dfb5c3e134d19414735dbcd7554925c00/suspicious.zip). Unzip the archive with the password `picoctf`

Additional details will be available after launching your challenge instance.

Once you have created the YARA rule/signature, submit your rule file as follows:`socat -t60 - TCP:standard-pizzas.picoctf.net:55185 < sample.txt`(In the above command, modify "sample.txt" to whatever filename you use).When you submit your rule, it will undergo testing with various test cases. If it successfully passes all the test cases, you'll receive your flag.
## Pistas

1. The test cases will attempt to match your rule with various variations of this suspicious file, including a packed version, an unpacked version, slight modifications to the file while retaining functionality, etc.
2. Since this is a Windows executable file, some strings within this binary can be "wide" strings. Try declaring your string variables something like `$str = "Some Text" wide ascii` wherever necessary.
3. Your rule should also not generate any false positives (or false negatives). Refine your rule to perfection! One YARA rule file can have multiple rules! Maybe define one rule for Packed binary and another rule for Unpacked binary in the same rule file?

## Solución

OmarSC-picoctf@webshell:~$ file suspicious.exe
suspicious.exe: PE32 executable (GUI) Intel 80386, for MS Windows, UPX compressed
OmarSC-picoctf@webshell:~$ strings suspicious.exe | grep -Ei "cmd|powershell|http|base64|exec|virtualalloc|shell"
        <requestedExecutionLevel level='asInvoker' uiAccess='false' />
SHELL32.dll
OmarSC-picoctf@webshell:~$ strings suspicious.exe | grep -Ei cmd|powershell|http|base64|exec|virtualalloc|shell 
-bash: powershell: command not found
-bash: http: command not found
-bash: virtualalloc: command not found
-bash: shell: command not found
OmarSC-picoctf@webshell:~$ strings suspicious.exe | grep -Ei pico                                              
OmarSC-picoctf@webshell:~$ strings suspicious.exe | grep -Ei cmd 
OmarSC-picoctf@webshell:~$ strings suspicious.exe | grep -Ei powershell
OmarSC-picoctf@webshell:~$ peinfo suspicious.exe
-bash: peinfo: command not found
OmarSC-picoctf@webshell:~$ readpe suspicious.exe -h
-bash: readpe: command not found
OmarSC-picoctf@webshell:~$ ^C
OmarSC-picoctf@webshell:~$ upx -d suspicious.exe
                       Ultimate Packer for eXecutables
                          Copyright (C) 1996 - 2020
UPX 3.96        Markus Oberhumer, Laszlo Molnar & John Reiser   Jan 23rd 2020

        File size         Ratio      Format      Name
   --------------------   ------   -----------   -----------
     40960 <-     26624   65.00%    win32/pe     suspicious.exe

Unpacked 1 file.
OmarSC-picoctf@webshell:~$ file suspicious.exe
suspicious.exe: PE32 executable (GUI) Intel 80386, for MS Windows
OmarSC-picoctf@webshell:~$ strings suspicious.exe | grep -Ei "cmd|powershell|http|base64|exec|virtualalloc|shell"
SHELL32.dll
        <requestedExecutionLevel level='asInvoker' uiAccess='false' />
OmarSC-picoctf@webshell:~$ objdump -p suspicious.exe | grep "DLL"
 vma:            Hint    Time      Forward  DLL       First
        DLL Name: KERNEL32.DLL
        DLL Name: ADVAPI32.dll
        DLL Name: api-ms-win-crt-convert-l1-1-0.dll
        DLL Name: api-ms-win-crt-heap-l1-1-0.dll
        DLL Name: api-ms-win-crt-locale-l1-1-0.dll
        DLL Name: api-ms-win-crt-math-l1-1-0.dll
        DLL Name: api-ms-win-crt-runtime-l1-1-0.dll
        DLL Name: api-ms-win-crt-stdio-l1-1-0.dll
        DLL Name: GDI32.dll
        DLL Name: SHELL32.dll
        DLL Name: USER32.dll
        DLL Name: VCRUNTIME140.dll
OmarSC-picoctf@webshell:~$ nano suspicious.yara
OmarSC-picoctf@webshell:~$ yara suspicious.yara suspicious.exe
-bash: yara: command not found
OmarSC-picoctf@webshell:~$ sudo apt update && sudo apt install yara -y
-bash: sudo: command not found
OmarSC-picoctf@webshell:~$ ^C
OmarSC-picoctf@webshell:~$ nano sample.txt                         
OmarSC-picoctf@webshell:~$ socat -t60 - TCP:standard-pizzas.picoctf.net:55185 < sample.txt
:::::

Status: Failed
False Negatives Check: Testcases passed!
False Positives Check: Testcase failed. Your rule generated a false positive.
Stats: 3 testcase(s) passed. 1 failed. 60 testcase(s) unchecked. 64 total testcases.
Pass all the testcases to get the flag.

:::::
OmarSC-picoctf@webshell:~$ nano sample.txt
OmarSC-picoctf@webshell:~$ socat -t60 - TCP:standard-pizzas.picoctf.net:55185 < sample.txt
:::::

Status: Failed
False Negatives Check: Testcases passed!
False Positives Check: Testcase failed. Your rule generated a false positive.
Stats: 3 testcase(s) passed. 1 failed. 60 testcase(s) unchecked. 64 total testcases.
Pass all the testcases to get the flag.

:::::
OmarSC-picoctf@webshell:~$ socat -t60 - TCP:standard-pizzas.picoctf.net:55185 < sample.txt
:::::

Status: Failed
False Negatives Check: Testcases passed!
False Positives Check: Testcase failed. Your rule generated a false positive.
Stats: 3 testcase(s) passed. 1 failed. 60 testcase(s) unchecked. 64 total testcases.
Pass all the testcases to get the flag.

:::::
OmarSC-picoctf@webshell:~$ nano sample.txt
OmarSC-picoctf@webshell:~$ nano sample.txt
OmarSC-picoctf@webshell:~$ socat -t60 - TCP:standard-pizzas.picoctf.net:64517 < sample.txt
:::::

Status: Failed
False Negatives Check: Testcase failed. Your rule generated a false negative.
False Positives Check: Testcase failed. Your rule generated a false positive.
Stats: 17 testcase(s) passed. 1 failed. 46 testcase(s) unchecked. 64 total testcases.
Pass all the testcases to get the flag.

:::::
OmarSC-picoctf@webshell:~$ strings suspicious.exe | grep -i "unique_string"
OmarSC-picoctf@webshell:~$ strings suspicious.exe | less
OmarSC-picoctf@webshell:~$ nano sample.txt
OmarSC-picoctf@webshell:~$ socat -t60 - TCP:standard-pizzas.picoctf.net:64517 < sample.txt
:::::

Status: Failed
False Negatives Check: Testcases passed!
False Positives Check: Testcase failed. Your rule generated a false positive.
Stats: 3 testcase(s) passed. 1 failed. 60 testcase(s) unchecked. 64 total testcases.
Pass all the testcases to get the flag.



## Notas Adicionales



## Referencias
- 

