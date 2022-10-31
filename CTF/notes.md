### crypto

#### from base64
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)


### for

#### stegonagraphy



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
