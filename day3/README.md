# datadog-fundamental_training

### Revision 1 

<img src="rev1.png">

### Revision understanding for custom metric 

<img src="rev2.png">

### final revision 

<img src="rev3.png">

### introduction to logging via datadog 

<img src="log1.png">

### by default logging is disabled -- veriy that

```
 cd  /etc/datadog-agent/
root@ip-172-31-90-155:/etc/datadog-agent# ls
auth_token    conf.d                install_info                 selinux
checks.d      datadog.yaml          runtime-security.d           system-probe.yaml.example
compliance.d  datadog.yaml.example  security-agent.yaml.example


root@ip-172-31-90-155:/etc/datadog-agent#
root@ip-172-31-90-155:/etc/datadog-agent# grep -in logs  datadog.yaml
36:## setting defined in "site". It does not affect APM, Logs or Live Process intake which have their
48:## For Logs proxy information, refer to https://docs.datadoghq.com/agent/proxy/#proxy-for-logs
568:  ## - logs_config.use_http
569:  ## - logs_config.logs_no_ssl
570:  ## - logs_config.logs_dd_url
611:  ## @param  logs - custom object - optional
612:  ## Specific configurations for logs
614:  # logs:
617:    ## @env DD_OBSERVABILITY_PIPELINES_WORKER_LOGS_ENABLED - boolean - optional - default: false
618:    ## Enables forwarding of logs to an Observability Pipelines Worker
623:    ## @env DD_OBSERVABILITY_PIPELINES_WORKER_LOGS_URL - string - optional - default: ""
624:    ## URL endpoint for the Observability Pipelines Worker to send logs to
1062:## @param logs_enabled - boolean - optional - default: false
1063:## @env DD_LOGS_ENABLED - boolean - optional - default: false
1064:## Enable Datadog Agent log collection by setting logs_enabled to true.
1**066:# logs_enabled: false**
```

### exam preferd answer 

```
 datadog-agent  status   |  grep -i logs
    config_logs_dd_url:
    config_logs_socks5_proxy_address:
    feature_logs_enabled: false
Logs Agent
  Logs Agent is not running
```




