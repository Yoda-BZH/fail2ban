fail2ban
========

personnal filters for fail2ban


ngircd
======

A rule for bad server password errors.

Configuration :
```
[ngircd]
enabled  = true
port     = 6667
filter   = ngircd
logpath  = /var/log/daemon.log
maxretry = 3
```

fail2ban-ssh
============

A rule for repeatedly banned hosts.

Configuration:
```
[fail2ban-ssh]
enabled  = true
filter   = fail2ban-ssh
logpath  = /var/log/fail2ban.log
maxretry = 3
# 3600 * 24 * 3
findtime = 259200
# 3600 * 24
bantime  = 86400
port     = ssh
```
