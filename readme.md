# Introduction

# Requequisite

# Setup

# Take note
## Apply power admin DNS
Change your /etc/resolv.conf into 
```conf
# This is /run/systemd/resolve/stub-resolv.conf managed by man:systemd-resolved(8).
# Do not edit.
#
# This file might be symlinked as /etc/resolv.conf. If you're looking at
# /etc/resolv.conf and seeing this text, you have followed the symlink.
#
# This is a dynamic resolv.conf file for connecting local clients to the
# internal DNS stub resolver of systemd-resolved. This file lists all
# configured search domains.
#
# Run "resolvectl status" to see details about the uplink DNS servers
# currently in use.
#
# Third party programs should typically not access this file directly, but only
# through the symlink at /etc/resolv.conf. To manage man:resolv.conf(5) in a
# different way, replace this symlink by a static file or a different symlink.
#
# See man:systemd-resolved.service(8) for details about the supported modes of
# operation for /etc/resolv.conf.

nameserver 127.0.0.53
## Depend on your setup
options edns0 trust-ad
search vyzxqwws12fuzean3kaeuvsfcc.hx.internal.cloudapp.net

```
Because _systemd-resolved_ will occupy port 53 by default. So, PowerDNS cannot use, cause that it cannot restart. You first stop _systemd-resolved_ and restart. Make sure that your database are available! 
`
## Mysql

> [!TIP]
> This mysql is fvckin trap, you better take a note to this point. The config for bind-address is the bellow !

```  
/etc/mysql/mysql.conf.d/mysqld.cnf
```



> [!NOTE]  
> Highlights information that users should take into account, even when skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]  
> Crucial information necessary for users to succeed.

> [!WARNING]  
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.