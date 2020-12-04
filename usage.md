Changes
===

# source
[wenkb's docker-ubuntu-ssh-vnc](https://github.com/wenkb/docker-ubuntu-ssh-vnc)

# history
## Dec/5, 2020, cchxx
- upgrade to ubuntu 20.04
- add soure of aliyun
- install build-essential
- uninstall gedit
- uninstall sublime text3

# build
```
$ docker build -t docker-ubuntu-ssh-vnc:test . 
```

# run
```
docker run --name ubuntudev  -itd -p 5900:5900 -p 22:22 -v ~/sharefolder:/mnt/sharefolder --privileged=true  --ulimit memlock=-1   docker-ubuntu-ssh-vnc:test
```
