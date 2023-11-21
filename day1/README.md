### Certification and training 

<img src="cert.png">

### SAAS model -- Datadog 

<img src="saas.png">

### datadog agent 

<img src="agent.png">

### Using datadog -- understanding basic subscription model 

<img src="model.png">

### Understanding lab env 

<img src="lab.png">


## Loging to ubuntu VM using ssh from windows Powershell

```
PS C:\Users\humanfirmware> cd .\Downloads\
PS C:\Users\humanfirmware\Downloads>
PS C:\Users\humanfirmware\Downloads> ssh  -i  ashu-datadog.pem   ubuntu@44.202.148.132
The authenticity of host '44.202.148.132 (44.202.148.132)' can't be established.
ED25519 key fingerprint is SHA256:pJGZrbZsRK/jW/cB9Czj3PN7uoWX5r+lB1hFfWa5XPs.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '44.202.148.132' (ED25519) to the list of known hosts.
Welcome to Ubuntu 22.04.3 LTS (GNU/Linux 6.2.0-1012-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

```

### verify login 

```
ubuntu@ip-172-31-90-155:~$ uname
Linux
ubuntu@ip-172-31-90-155:~$
ubuntu@ip-172-31-90-155:~$
ubuntu@ip-172-31-90-155:~$ whoami
ubuntu
```

