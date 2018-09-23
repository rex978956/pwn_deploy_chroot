# pwn_deploy_chroot

> A project for deploying ctf pwn challenge use chroot

中文请点击：

[README_CN.md](https://github.com/giantbranch/pwn_deploy_chroot/blob/master/README_CN.md)

## Before

```
# Install the latest version docker
curl -s https://get.docker.com/ | sh
# Install docker compose
apt install docker-compose
```

## Configuration

Put your pwn bin to ./bin （**Note that the filename should not contain special characters.**）

Listen port start from 10000, you can change in config.py

## Run

```
python initialize.py
# please run as root
docker-compose up --build -d
```

## Attention

The flag will be generated by the initialize.py and it store in flags.txt

The port information corresponding to the pwn program is also inside  flags.txt.

## Update

2018.09.17 version v1

2018.09.23 version v2：Use the catflag program instead of /bin/sh, which is more secure

## Reference

https://github.com/Eadom/ctf_xinetd
