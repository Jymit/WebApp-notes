#### IDOR (INSECURE DIRECT OBJECT REFERENCE) 
```
There can be many variables in the application such as “id”, “pid”, “uid”. Although these values are often seen as HTTP parameters, they can be found in headers and cookies. The attacker can access, edit or delete any of other users’ objects by changing the values. This vulnerability is called IDOR.
```

#### Effective & fast IDOR vulnerability test
- Burp Suite’s HTTP History tab for checking all of requests.
- filtering in the HTTP History tab by selecting “Show only in-scope items”.
- If you have all API requests of the application like WSDL file, Swagger page etc. and it’s working regularly, you’re in luck! You can use this and it’ll give you convenience for IDOR testing.
 
#### find injection points
- 

#### BLIND IDOR


#### 
- IDOR vulnerability allows us to access an account at some time, rather than to edit or delete it. These critical bugs appear in fields such as password reset, password change, account recovery. 
- HPP (HTTP Parameter Pollution) vulnerability for IDOR testing by adding the same parameter one more time in your request.


#### tools?
- Burp Suite. Extender, bApp store:
- Autorize https://github.com/portswigger/autorize
- AutoRepeater https://github.com/PortSwigger/auto-repeater
- https://youtu.be/3K1-a7dnA60?t=107
