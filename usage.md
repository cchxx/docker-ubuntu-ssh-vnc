Changes
===

# source
[wenkb's docker-ubuntu-ssh-vnc](https://github.com/wenkb/docker-ubuntu-ssh-vnc)

# history

## Dec/5, 2020, chx
- upgrade to ubuntu 20.04
- add soure of aliyun
- install build-essential
- uninstall gedit
- uninstall sublime text3

## Dec/13, 2020, chx
- change "startup.sh" to unix format
- add source of tsinghua
- install vim
- update usage for windows 10

# build
```
$ docker build -t docker-ubuntu-ssh-vnc:v0 . 
```

# run
```
docker run --name ubuntu-desk  -itd -p 5900:5900 -p 22:22 -v /hostfolder:/containerfolder --privileged=true  --ulimit memlock=-1   docker-ubuntu-ssh-vnc:v0
```

# for Windows 10

## issue for start a container on windows
If running on windows 10, please change CMD file format to unix.
For example, use vim command ":set ff=unix".

Otherwise, will hit issue 'standard_init_linux.go:211: exec user process caused "no such file or directory"' during contianer starting.

## mount windows folder for docker container
```
docker run --name ubuntu-desk  -itd -p 5900:5900 -p 22:22 -v ${PWD}:/containerfolder --privileged=true  --ulimit memlock=-1   docker-ubuntu-ssh-vnc:v1
```
