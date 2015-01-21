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

repeat-ssh
============

A rule for repeatedly banned hosts.

Configuration:
```
[repeat-ssh]
enabled  = true
filter   = repeat-ssh
logpath  = /var/log/fail2ban.log
maxretry = 3
# 3600 * 24 * 3
findtime = 259200
# 3600 * 24
bantime  = 86400
port     = ssh
```


permanent-ssh
==========

A Rule to ban far longer banned hosts from repeat-ssh

```
[permanent-ssh]
enabled  = true
filter   = permanent-ssh
logpath  = /var/log/fail2ban.log
maxretry = 3
findtime = 259200
# 3600 * 24 * 365
bantime  = 31536000
port     = ssh
```

