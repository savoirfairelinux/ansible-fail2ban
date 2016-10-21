Ansible Fail2ban Role
============

Easily edit and deploy simple Fail2ban service into your server on the fly with easy configuration.


System requirements
------------

* Ubuntu >= 12.04 or Debian >= 6
* Ansible 2.0+ installed on the host
* Vagrant 1.8.**4**+ (only needed for local deployments)
* sflvault (needed to fetch secrets)


Installation procedure
------------

Simply add this role into your Ansible file, change the config as your need, and then run provision.

```
---
- hosts: all
  roles:
    - role: fail2ban
      fail2ban_bantime: 600  # Ban time in seconds
      fail2ban_findtime: 30  # Interval of seconds in which X "maxretry" is allowed
      fail2ban_maxretry: 4   # Max retry possible into "findtime" interval before ban
```

