# ansible-snmpd

This is very early support of snmpd, support only few options.

## Requirements

* Ansible 2.5+;

## Example configuration

```yaml
---
# Enable snmpd service or not.
snmpd_enable: 'true'
# Restart snmpd after deploy or not.
snmpd_restart: 'true'
# Install snmpd package or not.
snmpd_install_package: 'true'

snmpd:
- system:
  - rocommunity: 'public'
    syslocation: '37 Riegelmann Boardwalk, Brooklyn, NY 11224, USA'
    syscontact: 'noc@opentech.ru'
  agent:
    - agentaddress: 'udp:161'
  extend:
  - "pi_cputemp /usr/bin/pi_cputemp"
```
