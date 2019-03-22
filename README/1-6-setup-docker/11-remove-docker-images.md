**Remove Docker Images.**

Check the Docker image list.
```bash
docker image ls -a
▶ REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
  ruby                latest              2d6f7a467f2c        9 days ago          870MB
```

Remove a Docker image using the Docker `REPOSITORY` name.
```bash
docker image rm ruby --force
▶ Untagged: ruby:latest
  Untagged: ruby@sha256:0048434fd0ea67f0c8fc5d959a38751fced429c3c80c28e293518486f9039723
  Deleted: sha256:2d6f7a467f2c491fded68ef2d743de817b01a92fc22bbbdc0520a44ed5b9e37b
```

Check the Docker image list.
```bash
docker image ls -a
▶ REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
```

Remove all unused Docker containers.
```bash
docker image prune
▶ WARNING! This will remove all dangling images.
  Are you sure you want to continue? [y/N] y
  Total reclaimed space: 0B
```
