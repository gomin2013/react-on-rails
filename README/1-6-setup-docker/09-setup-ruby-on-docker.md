**Setup Ruby on Docker.**

![Setup Ruby on Docker](/README/images/1-6-setup-ruby-on-docker.png)

Download the `Ruby` as a Docker image form the `Docker Hub`.
```bash
docker pull ruby
▶ Using default tag: latest
  latest: Pulling from library/ruby
  22dbe790f715: Pull complete
  0250231711a0: Pull complete
  6fba9447437b: Pull complete
  c2b4d327b352: Pull complete
  270e1baa5299: Pull complete
  01cbe6152974: Pull complete
  007613428043: Pull complete
  ae0982fbaa0b: Pull complete
  Digest: sha256:0048434fd0ea67f0c8fc5d959a38751fced429c3c80c28e293518486f9039723
  Status: Downloaded newer image for ruby:latest
```

Check the `Ruby` Docker image on the Docker image list.
```bash
docker images -a
▶ REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
  ruby                latest              2d6f7a467f2c        9 days ago          870MB
```

![Optional](/README/images/optional.png) Check the Docker container list.
```bash
docker container ps -a
▶ CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
```
It's empty because you haven't run any Docker image commands yet.
<br>
<br>
