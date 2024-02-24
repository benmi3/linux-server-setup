# Crowdsec setup **UNTESTED**

This is mainly focused at EL/Centos stream 8/ fedora*

Source: [docs](https://docs.crowdsec.net/docs/getting_started/install_crowdsec/)
## Install Guide

First install repos
```bash
curl -s https://packagecloud.io/install/repositories/crowdsec/crowdsec/script.rpm.sh | sudo bash
```
Install the security engine 
```bash
dnf install crowdsec
```
Install [Remedation Component](https://docs.crowdsec.net/u/bouncers/intro/)
```bash
dnf install crowdsec-firewall-bouncer-iptables
```

## Crowdsec configuration

Default config should be in /etc/crowdsec/config.yaml
Create new configfile in same folder called `config.yaml.local`
This is to keep the config file during upgrades.
### Configuration files that support `.yaml.local`
- `config.yaml`
- `local_api_credentials.yaml`
- `simulation.yaml`
- `bouncers/crowdsec-firewall-bouncer.yaml`
- `bouncers/crowdsec-custom-bouncer.yaml`
- `bouncers/crowdsec-blocklist-mirror.yaml`
### config.yaml.local
```yaml
common:
  log_level: info

db_config:
  log_level: info
  db_config:
  type:     mysql
  user:     database_user
  password: ${DB_PASSWORD}
  db_name:  db_name
  host:     192.168.0.2
  port:     3306
  flush:
    max_items: 5000
    max_age: 7d
    #bouncers_autodelete:
    #  cert: 7d
    #  api_key: 7d
    #agents_autodelete:
    #  cert: 7d
    #  login_password: 7d
api:
  client:
    insecure_skip_verify: false
    credentials_path: /etc/crowdsec/local_api_credentials.yaml
  server:
    enable: true
    log_level: info
    listen_uri: 127.0.0.1:8080
    profiles_path: /etc/crowdsec/profiles.yaml
    use_forwarded_for_headers: false
    console_path: /etc/crowdsec/console.yaml
    online_client: # Crowdsec API
      credentials_path: /etc/crowdsec/online_api_credentials.yaml
#    capi_whitelists_path: /etc/crowdsec/capi_whitelists.yaml
#    tls:
#      cert_file: /etc/crowdsec/ssl/cert.pem
#      key_file: /etc/crowdsec/ssl/key.pem
#      client_verification: "VerifyClientCertIfGiven"
#      ca_cert_path: /path/to/ca.crt
#      agents_allowed_ou: # List of allowed Organisational Unit for the agents
#       - agents_ou
#      bouncers_allowed_ou: # List of allowed Organisational Unit for the bouncers
#       - bouncers_ou
#      crl_path: /path/to/file.crl
#      cache_expiration: 1h
prometheus:
  enabled: true
  level: full
  listen_addr: 127.0.0.1
  listen_port: 6060
```
## Enviromental
Put this in `/etc/enviroment`. But this will need root/sudo perms.
```bash
export DB_PASSWORD="<db_password>"
```