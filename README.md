Ansible Fail2ban Role
============

Easily edit and deploy simple Fail2ban service into your server on the fly with easy configuration.


System requirements
------------

* Ubuntu 16.04 or Debian 8
* Ansible 2.0+ installed on the host


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

