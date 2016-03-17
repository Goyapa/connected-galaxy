```bash
michael@mjm:~$ hostname -I
192.168.2.128 172.17.0.1 
michael@mjm:~$ nmap -sP 192.168.2.128/24 | grep black-pearl
Nmap scan report for black-pearl.speedport.ip (192.168.2.141)

michael@mjm:~$ ssh root@192.168.2.141
root@192.168.2.141's password:
HypriotOS: root@black-pearl in ~
$ ls
firstboot.sh  firstboot_done
HypriotOS: root@black-pearl in ~
$ docker info
Containers: 0
Images: 8
Server Version: 1.9.0
Storage Driver: overlay
 Backing Filesystem: extfs
Execution Driver: native-0.2
Logging Driver: json-file
Kernel Version: 4.1.12-hypriotos+
Operating System: Raspbian GNU/Linux 8 (jessie)
CPUs: 1
Total Memory: 434.2 MiB
Name: black-pearl
Debug mode (server): true
 File Descriptors: 14
 Goroutines: 25
 System Time: 2016-03-17T14:56:38.675398141+01:00
 EventsListeners: 0
 Init Path: /usr/lib/docker/dockerinit
 Docker Root Dir: /var/lib/docker
HypriotOS: root@black-pearl in ~

$ docker pull hypriot/rpi-node
Using default tag: latest
latest: Pulling from hypriot/rpi-node
44699884a001: Pull complete 
6a919eace64a: Pull complete 
35420324a82b: Pull complete 
03eb91f6ed4e: Pull complete 
4b9daf188fb3: Pull complete 
aa5bde53132a: Pull complete 
21cadd0bbdce: Pull complete 
f150252bc021: Pull complete 
e9e987a6b76b: Pull complete 
4816796b8487: Pull complete 
9e4e44755649: Pull complete 
3a41ec14ed77: Pull complete 
54e8ceab56d5: Pull complete 
5165481d2ac6: Pull complete 
Status: Downloaded newer image for hypriot/rpi-node:latest
HypriotOS: root@black-pearl in ~

$ docker run -i -t hypriot/rpi-node /bin/bash
root@7b7e2272b964:/# node -v
v5.8.0
root@7b7e2272b964:/# ps
  PID TTY          TIME CMD
    1 ?        00:00:01 bash
   16 ?        00:00:00 ps
root@7b7e2272b964:/# nvm
bash: nvm: command not found
root@7b7e2272b964:/# node -v
v5.8.0
root@7b7e2272b964:/# npm -v
3.7.3
root@7b7e2272b964:/# ls
bin   dev  home  media	opt   root  sbin  sys  usr
boot  etc  lib	 mnt	proc  run   srv   tmp  var

```
