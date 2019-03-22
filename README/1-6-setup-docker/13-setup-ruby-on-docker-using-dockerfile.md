**Setup Ruby on Docker using Dockerfile.**

![Ruby Docker Image](/README/images/1-6-dockerfile-logo.png)

Create a project directory. `react-on-rails` is the project name.
```bash
mkdir react-on-rails
```

Open the directory.
```bash
cd react-on-rails
```

Create a `Dockerfile` inside the project directory.
```bash
touch Dockerfile
```

Dockerfile
```docker
FROM ruby
```

Run the `Dockerfile` to install the Ruby Docker image.
```bash
docker build .
▶ Sending build context to Docker daemon  19.01MB
  Step 1/1 : FROM ruby
  latest: Pulling from library/ruby
  22dbe790f715: Already exists
  0250231711a0: Already exists
  6fba9447437b: Already exists
  c2b4d327b352: Already exists
  270e1baa5299: Already exists
  01cbe6152974: Already exists
  007613428043: Already exists
  ae0982fbaa0b: Already exists
  Digest: sha256:0048434fd0ea67f0c8fc5d959a38751fced429c3c80c28e293518486f9039723
  Status: Downloaded newer image for ruby:latest
   ---> 2d6f7a467f2c
  Successfully built 2d6f7a467f2c
```

Check `Successfully built 2d6f7a467f2c` on the Docker image list.
```bash
docker image ls -a
▶ REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
  ruby                latest              2d6f7a467f2c        9 days ago          870MB
```

Check `Ruby` & `Gem` version on Docker with the `--rm` option.
```bash
docker run --rm ruby ruby -v
▶ ruby 2.6.2p47 (2019-03-13 revision 67232) [x86_64-linux]

docker run --rm ruby gem -v
▶ 3.0.3
```
The `--rm` option will prevent creating unused containers.

Check the Docker container list.
```bash
docker container ps -a
▶ CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
```
