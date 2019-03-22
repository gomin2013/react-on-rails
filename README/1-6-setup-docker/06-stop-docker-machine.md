**Stop Docker Machine.**

Stop the `default` Docker Machine.
```bash
docker-machine stop
▶ Stopping "default"...
  Machine "default" was stopped.
```

Check Docker Machine list.
```bash
docker-machine ls
▶ NAME      ACTIVE   DRIVER       STATE     URL   SWARM   DOCKER    ERRORS
  default   -        virtualbox   Stopped                 Unknown
```

![Optional](/README/images/optional.png) Check running virtual machine list.
```bash
vboxmanage list runningvms
▶
```
![Optional](/README/images/optional.png) Check the virtual machine status on the `VirtualBox` app.

![Docker Machine was stopped](/README/images/1-6-docker-machine-was-stopped.png)
<br>
