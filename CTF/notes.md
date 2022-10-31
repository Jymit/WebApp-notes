### crypto

#### from base64
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)


### for

#### stegonagraphy

#### disasm
- disassembly of file to find flags v1, v2 for grepping thru the needful output
```
#!/bin/bash

echo "Attempting disassembly of $1 ..."


#This usage of "objdump" disassembles all (-D) of the first file given by 
#invoker, but only prints out the ".text" section (-j .text) (only section
#that matters in almost any compiled program.

objdump -Dj .text $1 > $1.ltdis.x86_64.txt

#Check that $1.ltdis.x86_64.txt is non-empty
#Continue if it is, otherwise print error and eject

if [ -s "$1.ltdis.x86_64.txt" ]
then
	echo "Disassembly successful! Available at: $1.ltdis.x86_64.txt"

	echo "Ripping strings from binary with file offsets..."
	strings -a -t x $1 > $1.ltdis.strings.txt
	echo "Any strings found in $1 have been written to $1.ltdis.strings.txt with file offset"

else
	echo "Disassembly failed!"
	echo "Usage: ltdis.sh <program-file>"
	echo "Bye!"
fi
```



### webapp

#### SQLi

SELECT * FROM users WHERE username='''

SELECT * FROM users WHERE username='' OR 1=1

SELECT * FROM users WHERE username=''-- '

#### Directory Traversal

#### Command Injection

#### Cross Site Request Forgery or CSRF

#### Cross Site Scripting or XSS 

Reflected XSS
https://ctfmadeurl.org/?data=%3Cscript%3Ealert(1)%3C/script%3E

Stored XSS

DOM XSS

#### Server Side Request Forgery or SSRF


##### Server-Side Template Injection or SSTI

https://portswigger.net/research/server-side-template-injection

#### quip enum
$ git clone https://github.com/quip/quip-api.git
$ cd quip-api/samples/baqup/
$ python main.py --access_token="abcdefghijklmnopqrstuvwxyz" --quip_api_base_url="https://platform.quip-hosted.com" --output_directory=CTF
