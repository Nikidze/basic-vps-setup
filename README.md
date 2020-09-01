# Basic Vps Setup
The basic vps setup tutorial

## Create www user
First, connect to your vps and create a new user. Then, give it a password and add it to sudo group.
```
adduser www
usermod -aG sudo username
```
Disconnect from VPn by typing exit.

```
exit
```

## Automatic SSH authentication by key

```
mkdir ~/.ssh
ssh-keygen -t rsa -q -N '' -f ~/.ssh/id_rsa
ssh-copy-id -i ~/.ssh/id_rsa.pub www@your-domain-or-ip
```

