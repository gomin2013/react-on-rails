**Remove Docker Containers.**

Check the Docker container list.
```bash
docker container ps -a
▶ CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS                          PORTS               NAMES
  24501bea4531        ruby                "ls"                6 seconds ago       Exited (0) 6 seconds ago                        reverent_poitras
  193ce9d4129d        ruby                "gem -v"            21 seconds ago      Exited (0) 21 seconds ago                       friendly_wescoff
  e364803ca9f4        ruby                "ruby -v"           31 seconds ago      Exited (0) 30 seconds ago                       agitated_tu
  056829fab166        2d6f7a467f2c        "gem -v"            49 seconds ago      Exited (0) 48 seconds ago                       dreamy_lehmann
  47fe038aac8f        2d6f7a467f2c        "ruby -v"           53 seconds ago      Exited (0) 53 seconds ago                       affectionate_feynman
```

Remove all unused Docker containers.
```bash
docker container prune
▶ WARNING! This will remove all stopped containers.
  Are you sure you want to continue? [y/N] y
  Deleted Containers:
  24501bea4531bda17fe5e5e2bc6d22ae52c6692ec78bfadf6f184689c076036b
  193ce9d4129dfe077213614fc3a5219c9b14ab127892ad5230d17119d5f6c5c4
  e364803ca9f4eb49bd854affbceda1f4eef930d6e47c123288fbcab6f78a8877
  056829fab1662f33a5ef5777adc323aabd97632ca2fd7d00529146eaac8efbfa
  47fe038aac8f062df8c5e8b5638454826c432cff65d9bd7b34fca6be0b0ce5df
  
  Total reclaimed space: 0B
```

Check the Docker container list.
```bash
docker container ps -a
▶ CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
```
