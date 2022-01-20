
# test_service.service
```
[Unit]
Description=First daemon service
#Requires=syslog.socket
Documentation=none
Documentation=Test first daemon

[Service]
Type=simple
ExecStart=/home/scott/prj/daemon_test/daemon-skeleton-linux-c/a.out
StandardOutput=null
Restart=on-failure

# Increase the default a bit in order to allow many simultaneous
# files to be monitored, we might need a lot of fds.
#LimitNOFILE=16384

[Install]
WantedBy=multi-user.target
#Alias=syslog.service
```

# softlink to
```
/etc/systemd/system/test_service.service -> /<path>/test_service.service
```

# systemctl
  ```
  systemctl enable test_service
  systemctl start test_service
  systemctl status test_service
  systemctl status --no-pager test_service // do not wait log
  systemctl stop test_service
  ```
