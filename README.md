# Basic Vps Setup
The basic vps setup tutorial

## Automatic SSH authentication by key (run localy)

```
ssh-copy-id -i ~/.ssh/id_rsa.pub root@your-domain-or-ip
```

## Change SSH port to ${some port}

```
nano /etc/ssh/sshd_config
Port ${some port}
/sbin/iptables -A INPUT -m state --state NEW -m tcp -p tcp --dport ${some port} -j ACCEPT
service ssh restart
```

