**Create and set a working directory on Dockerfile.**

Add the `RUN mkdir` instruction to create a project directory inside `Dockerfile`.
```dockerfile
RUN mkdir /react-on-rails
```

Add the `WORKDIR` instruction to set the directory as a working directory inside `Dockerfile`.
```dockerfile
WORKDIR /react-on-rails
```

Dockerfile
```dockerfile
FROM ruby

RUN mkdir /react-on-rails
WORKDIR /react-on-rails
```
`react-on-rails` is the project name.

Run the `Dockerfile`.
```bash
docker build .
▶ Sending build context to Docker daemon  19.07MB
  Step 1/3 : FROM ruby
   ---> 2d6f7a467f2c
  Step 2/3 : RUN mkdir /react-on-rails
   ---> Running in 8846ad2ae887
  Removing intermediate container 8846ad2ae887
   ---> 393dea77ded4
  Step 3/3 : WORKDIR /react-on-rails
   ---> Running in 19d3107ca84d
  Removing intermediate container 19d3107ca84d
   ---> 68ccc5824c62
  Successfully built 68ccc5824c62
```

Check the Docker image list.
```bash
docker image ls -a
▶ REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
  <none>              <none>              393dea77ded4        About an hour ago   870MB
  <none>              <none>              68ccc5824c62        About an hour ago   870MB
  ruby                latest              2d6f7a467f2c        9 days ago          870MB
```

Check directory list at the `Step 2/3 : RUN mkdir /react-on-rails` using the Docker image's id.
```diff
docker run --rm 393dea77ded4 ls
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
+ react-on-rails
  root
  run
  sbin
  srv
  sys
  tmp
  usr
  var
```
