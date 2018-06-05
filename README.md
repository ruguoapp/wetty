Wetty = Web + tty
-----------------

Terminal over HTTP and HTTPS. Wetty is an alternative to
ajaxterm/anyterm but much better than them because wetty uses ChromeOS'
terminal emulator (hterm) which is a full fledged implementation of
terminal emulation written entirely in Javascript. Also it uses
websockets instead of Ajax and hence better response time.

hterm source - https://chromium.googlesource.com/apps/libapps/+/master/hterm/

![Wetty](/terminal.png?raw=true)

Dockerized Version
------------------

This repo includes a Dockerfile you can use to run a Dockerized version of wetty.  You can run
whatever you want!

Just do:

```
    docker build -t docker.in.ruguoapp.com/wetty:latest --force-rm .
```

```
    docker push docker.in.ruguoapp.com/wetty:latest
```

```
    docker pull docker.in.ruguoapp.com/wetty:latest
```

```
    docker run --name wetty-server -p 3000:3000 -e sshhost="yourhost" -t docker.in.ruguoapp.com/wetty:latest
```

Visit the appropriate URL in your browser (`[localhost|$(boot2docker ip)]:PORT`).