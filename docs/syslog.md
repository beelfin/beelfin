# in the code
```
openlog ("firstdaemon", LOG_PID, LOG_LOCAL4);
syslog (LOG_NOTICE, "First daemon started.");
syslog (LOG_NOTICE, "First daemon terminated.");
closelog();
```

# /etc/rsyslog.conf
```
local4.*        /var/log/firstdaemon
```

# 참고 사이트
https://ahyuo79.blogspot.com/2019/04/syslog.html
