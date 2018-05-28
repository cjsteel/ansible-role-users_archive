# determining-gid-ranges.md
#

In order to determine group ID ranges on a particular system do something like:

```shell
cat /etc/login.defs | grep GID
```

In other words

```shell
# for target systems configured GID ranges
# 
# Regular groups:
#
# GID_MIN
# GID_MAX
#
# System groups:
#
# SYS_GID_MIN
# SYS_GID_MAX
```
