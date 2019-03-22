**Start Docker Machine.**

Start the `default` Docker Machine.
```bash
docker-machine start
▶ Starting "default"...
  (default) Check network to re-create if needed...
  (default) Waiting for an IP...
  Machine "default" was started.
  Waiting for SSH to be available...
  Detecting the provisioner...
  Started machines may have new IP addresses. You may need to re-run the `docker-machine env` command.
```

Check Docker Machine list.
```bash
docker-machine ls
▶ NAME      ACTIVE   DRIVER       STATE     URL                         SWARM   DOCKER     ERRORS
  default   *        virtualbox   Running   tcp://192.168.99.100:2376           v18.09.3
```

![Optional](/README/images/optional.png) Check running virtual machine list.
```bash
vboxmanage list runningvms
▶ "default" {eddc73af-e6cf-41bc-b67e-7c9c9f6cdaad}
```

![Optional](/README/images/optional.png) Check the virtual machine status on the `VirtualBox` app.

![Docker Machine is running](/README/images/1-6-docker-machine-is-running.png)

![Optional](/README/images/optional.png) Restart the `default` Docker Machine.
```bash
docker-machine restart
```
