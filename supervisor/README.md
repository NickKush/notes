# Supervidor

**Supervisor** - is a client/server system that allows its users to monitor and control a number of processes on UNIX-like operating systems.

[*Documentation*](http://supervisord.org/)

[*Github*](https://github.com/Supervisor/supervisor)

---

## Table of content

- [Supervidor](#supervidor)
  - [Table of content](#table-of-content)
  - [Cheet sheets](#cheet-sheets)
    - [Installing](#installing)
    - [Config file](#config-file)
    - [Update service configurations](#update-service-configurations)
    - [Service status](#service-status)
    - [Service start](#service-start)
    - [Service stop](#service-stop)
    - [Service restart](#service-restart)

---

## Cheet sheets

### Installing  

*Debian/Ubuntu*
```console
$ sudo apt install supervisor
```

### Config file

Default config files are stored on path:

```
/etc/supervisor/conf.d/
```

Usually config file end with `*.conf`

*Config file example*

```console
[program:%my-app-name%]
directory = /srv/myapp/
command = /srv/myapp/app

numprocs=1

stdout_logfile=/var/log/supervisor/myapp.log
stdout_logfile_maxbytes=50MB

stderr_logfile=/var/log/supervisor/myapp-err.log
stderr_logfile_maxbytes=50MB

autostart = true
autorestart = true

user = root

stopasgroup = true
stopsignal = QUIT
```

[**More about configuration files**](http://supervisord.org/configuration.html)

### Update service configurations

```console
$ sudo supervisorctl reread
$ sudo supervisorctl update
```

### Service status

If we need to check a certain service we can do it using the following command.

```console
$ sudo supervisorctl status %service_name%
```

If we need to check all services, then we can do the follow.

```console
$ sudo supervisorctl status all
```

### Service start

```console
$ sudo supervisorctl start %service_name% 
```

If we need to start all services, then we can do the following command.

```console
$ sudo supervisorctl start all
```

### Service stop

```console
$ sudo supervisorctl stop %service_name% 
```

If we need to stop all services, then we can do the following command.

```console
$ sudo supervisorctl stop all
```

### Service restart

```console
$ sudo supervisorctl restart %service_name% 
```

If we need to restart all services, then we can do the following command.

```console
$ sudo supervisorctl restart all
```