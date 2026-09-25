# Automatic reboot mikrotik

## Script
```bash
system script

```

```bash
add dont-require-permissions=no name=automatic_reboot owner=suporte policy=\
    ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon source=\
    "system reboot\r\
    \ny\r\
    \n"

```

## Scheduler
```bash
system scheduler

```

```bash
add interval=1d name=schedule_automatic_reboot on-event=\
    schedule_automatic_reboot policy=\
    ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon \
    start-date=feb/25/2024 start-time=04:00:00

```


