**Connect each shell session to Docker Machine.**

If your shell sessions haven't connected to the Docker Machine yet.<br>
When you run a docker command, you will get the warning message like below.
```bash
docker info
▶ Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?
```

Connect each shell session to the `default` Docker Machine.
```bash
eval "$(docker-machine env default)"
```
`default` is a name of the Docker Machine.

Check the Docker Machine connection by running the docker command again.
```bash
docker info
▶ Containers: 0
   Running: 0
   Paused: 0
   Stopped: 0
   ...
```

![Connect each shell session to Docker Machine](/README/images/1-6-connect-each-shell-session-to-docker-machine.gif)
<br>
<br>
