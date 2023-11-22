# datadog-fundamental_training

## revision 

<img src="rev.png">

### hands-on revision 

### checking linux host details 

```
ubuntu@ip-172-31-90-155:~$ whoami
ubuntu
ubuntu@ip-172-31-90-155:~$ uname
Linux
ubuntu@ip-172-31-90-155:~$ uname -r
6.2.0-1012-aws
ubuntu@ip-172-31-90-155:~$ cat  /etc/os-*
PRETTY_NAME="Ubuntu 22.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.3 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
```

### checking agent status

```
ubuntu@ip-172-31-90-155:~$ whoami
ubuntu
ubuntu@ip-172-31-90-155:~$
ubuntu@ip-172-31-90-155:~$ sudo  systemctl status datadog-agent
● datadog-agent.service - Datadog Agent
     Loaded: loaded (/lib/systemd/system/datadog-agent.service; enabled; vendor preset: enabled)
     Active: active (running) since Tue 2023-11-21 17:22:30 UTC; 11h ago
   Main PID: 19980 (agent)
      Tasks: 9 (limit: 4667)
     Memory: 87.1M
        CPU: 5min 43.732s
     CGroup: /system.slice/datadog-agent.service
             └─19980 /opt/datadog-agent/bin/agent/agent run -p /opt/datadog-agent/run/agent.pid
```

### alternativ

```
 sudo  service datadog-agent status
● datadog-agent.service - Datadog Agent
     Loaded: loaded (/lib/systemd/system/datadog-agent.service; enabled; vendor preset: enabled)
     Active: active (running) since Tue 2023-11-21 17:22:30 UTC; 11h ago
   Main PID: 19980 (agent)
      Tasks: 9 (limit: 4667)
     Memory: 87.5M
        CPU: 5min 44.104s
     CGroup: /system.slice/datadog-agent.service
             └─19980 /opt/datadog-agent/bin/agent/agent run -p /opt/datadog-agent/run/agent.pid
```

### final way to check datadog agent status

```
 datadog-agent status
Getting the status from the agent.


===============
Agent (v7.49.1)
===============

  Status date: 2023-11-22 04:40:30.846 UTC (1700628030846)
  Agent start: 2023-11-21 17:22:30.464 UTC (1700587350464)
  Pid: 19980
  Go Version: go1.20.10
  Python Version: 3.9.18
  Build arch: amd64
  Agent flavor: agent
  Check Runners: 4
  Log Level: info

  Paths
  =====
```


### checking config file 

```
 cd   /etc/datadog-agent/
root@ip-172-31-90-155:/etc/datadog-agent# ls
auth_token    conf.d                install_info                 selinux
checks.d      datadog.yaml          runtime-security.d           system-probe.yaml.example
compliance.d  datadog.yaml.example  security-agent.yaml.example
root@ip-172-31-90-155:/etc/datadog-agent#
```
