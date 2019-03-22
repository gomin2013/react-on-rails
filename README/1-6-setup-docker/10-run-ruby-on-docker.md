**Run Ruby on Docker.**

![Run Ruby on Docker](/README/images/1-6-run-ruby-on-docker.png)

Check `Ruby` & `Gem` version using `IMAGE ID`.
```bash
docker run 2d6f7a467f2c ruby -v
▶ ruby 2.6.2p47 (2019-03-13 revision 67232) [x86_64-linux]

docker run 2d6f7a467f2c gem -v
▶ 3.0.3
```

![Optional](/README/images/optional.png) Check the Docker container list after ran the Docker image commands above.
```bash
docker container ps -a
▶ CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
  202ae09b09cf        2d6f7a467f2c        "gem -v"            7 seconds ago       Exited (0) 7 seconds ago                        mystifying_northcutt
  acf0e1b91aba        2d6f7a467f2c        "ruby -v"           14 seconds ago      Exited (0) 14 seconds ago                       pensive_benz
```

![Optional](/README/images/optional.png) Check `Ruby` & `Gem` version using the Docker `REPOSITORY` name.
```bash
docker run ruby ruby -v
▶ ruby 2.6.2p47 (2019-03-13 revision 67232) [x86_64-linux]

docker run ruby gem -v
▶ 3.0.3
```

![Optional](/README/images/optional.png) Check the Docker container list after ran the Docker image commands above.
```bash
docker container ps -a
▶ CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS                      PORTS               NAMES
  91d06df1140a        ruby                "gem -v"            5 seconds ago        Exited (0) 4 seconds ago                        adoring_lalande
  bb2e30b79a99        ruby                "ruby -v"           10 seconds ago       Exited (0) 9 seconds ago                        eloquent_mcnulty
  202ae09b09cf        2d6f7a467f2c        "gem -v"            53 seconds ago       Exited (0) 52 seconds ago                       mystifying_northcutt
  acf0e1b91aba        2d6f7a467f2c        "ruby -v"           About a minute ago   Exited (0) 59 seconds ago                       pensive_benz
```

![Optional](/README/images/optional.png) Check directory list inside the Docker image.
```bash
docker run ruby ls
▶ bin
  boot
  dev
  etc
  home
  lib
  lib64
  media
  mnt
  opt
  proc
  root
  run
  sbin
  srv
  sys
  tmp
  usr
  var
```

![Optional](/README/images/optional.png) Check the Docker container list after ran the Docker image commands above.
```
docker container ps -a
▶ CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS                          PORTS               NAMES
  ef8bdc481b50        ruby                "ls"                4 seconds ago        Exited (0) 4 seconds ago                            zen_bassi
  91d06df1140a        ruby                "gem -v"            About a minute ago   Exited (0) About a minute ago                       adoring_lalande
  bb2e30b79a99        ruby                "ruby -v"           About a minute ago   Exited (0) About a minute ago                       eloquent_mcnulty
  202ae09b09cf        2d6f7a467f2c        "gem -v"            2 minutes ago        Exited (0) About a minute ago                       mystifying_northcutt
  acf0e1b91aba        2d6f7a467f2c        "ruby -v"           2 minutes ago        Exited (0) 2 minutes ago                            pensive_benz
```
