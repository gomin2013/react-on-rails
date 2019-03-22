![Rails + React + Webpack](/README/images/index.png)

# React on Rails

Integration of React (a JavaScript library) on Rails (a Ruby framework).

## 1 Setting up.

### 1.1 Install Homebrew.

![Homebrew](/README/images/1-1-homebrew-logo.png)

Install the `Homebrew` using the built-in Ruby.
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Check the `Homebrew` version.
```
brew -v
▶ Homebrew 2.1.0
  Homebrew/homebrew-core (git revision 5d5f; last commit 2019-04-07)
  Homebrew/homebrew-cask (git revision a2ad; last commit 2019-04-08)
```

![Optional](/README/images/optional.png) Check your system for potential problems.
```
brew doctor
▶ Your system is ready to brew.
```

![Optional](/README/images/optional.png) Update the `Homebrew` itself.
```
brew update
```

![Optional](/README/images/optional.png) Upgrade all outdated software packages.
```
brew upgrade
```

![Optional](/README/images/optional.png) Clean up everything at once.
```
brew cleanup
```

### 1.2 Install Ruby.

![Ruby](/README/images/1-2-ruby-logo.png)

**Built-in Ruby on Mac**

![Optional](/README/images/optional.png) Check `Ruby` & `Gem` version.
```
ruby -v
▶ ruby 2.3.7p456 (2018-03-28 revision 63024) [universal.x86_64-darwin18]

gem -v
▶ 2.5.2.3
```

![Optional](/README/images/optional.png) Check `Ruby`'s source directory.
```
which ruby
▶ /usr/bin/ruby
```
**Install Rbenv**

![Rbenv](/README/images/1-2-rbenv-logo.png)

Install the `rbenv` on Mac using the `Homebrew`.
```
brew install rbenv
```

Check the `rbenv` version.
```
rbenv -v
▶ rbenv 1.1.1
```

Check the `ruby-build` version.
```
ruby-build --version
▶ ruby-build 20190320
```
**Upgrade Ruby using Rbenv**

Check `Ruby` available versions in `rbenv` list.
```
rbenv install --list
▶ Available versions:
    ...
    ...
    2.6.2
    2.7.0-dev
    jruby-1.5.6
    ...
    ...
```

![Check Ruby available versions in rbenv list](/README/images/1-2-check-ruby-available-versions-in-rbenv-list.gif)

Install the `Ruby` specific version.
```
rbenv install 2.7.0-dev
```

Apply the `Ruby` version.
```
rbenv global 2.7.0-dev
rbenv rehash
```

Check `Ruby` & `Gem` version.
```
ruby -v
▶ ruby 2.7.0dev (2019-03-20 trunk 67314) [x86_64-darwin18]

gem -v
▶ 3.1.0.pre1
```

Check the `Ruby`'s source directory.
```
which ruby
▶ /Users/ab-watthajak/.rbenv/shims/ruby
```
**Uninstall Rbenv**

Uninstall both `rbenv` & `ruby-build` using the `Homebrew`.
```
brew remove rbenv ruby-build
▶ Uninstalling /usr/local/Cellar/rbenv/1.1.1... (36 files, 62.8KB)
  Uninstalling /usr/local/Cellar/ruby-build/20190314... (438 files, 219.7KB)
```

Remove the `rbenv`'s source directory.
```
rm -rf ~/.rbenv
```

Check the `Ruby`'s source directory.
```
which ruby
▶ /usr/bin/ruby
```

Check executable paths on Mac.
```
echo $PATH
▶ /Users/ab-watthajak/.rbenv/shims:/usr/local/opt/rbenv/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

Check executable paths after restart the iTerm.
```
echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```
**Install RVM**

![RVM](/README/images/1-2-rvm-logo.png)

Install `RVM` included `Ruby` using `curl`.
```
curl -sSL https://get.rvm.io | bash
```

Restart the iTerm and then check the `RVM`'s version.
```
rvm -v
▶ rvm 1.29.7-next (master) by Michal Papis, Piotr Kuczynski, Wayne E. Seguin [https://rvm.io]
```

![Optional](/README/images/optional.png) Enable `RVM` auto-update.
```
echo rvm_autoupdate_flag=2 >> ~/.rvmrc
```

![Optional](/README/images/optional.png) Update all rubies and gemsets.
```
rvm gemset update
```

Check `Ruby` versions on `RVM` list.
```
rvm list rubies
▶ # No rvm rubies installed yet. Try 'rvm help install'.
```

Check `Ruby` & `Gem` version.
```
ruby -v
▶ ruby 2.3.7p456 (2018-03-28 revision 63024) [universal.x86_64-darwin18]

gem -v
▶ 2.5.2.3
```
**Upgrade Ruby using RVM**

Install a new version of `Ruby` to `RVM` list.
```
rvm install ruby
```

Check `Ruby` versions on `RVM` list.
```
rvm list rubies
▶ => ruby-2.6.2 [ x86_64 ]

  # Default ruby not set. Try 'rvm alias create default <ruby>'.

  # => - current
  # =* - current && default
  #  * - default
```

Set the `Ruby` version as default.
```
rvm use ruby-2.6.2 --default
▶ Using /Users/ab-watthajak/.rvm/gems/ruby-2.6.2
```

check `Ruby` versions again on `RVM` list.
```
rvm list rubies
▶ =* ruby-2.6.2 [ x86_64 ]
  
  # => - current
  # =* - current && default
  #  * - default
```

Check `Ruby` & `Gem` version.
```
ruby -v
▶ ruby 2.6.2p47 (2019-03-13 revision 67232) [x86_64-darwin18]

gem -v
▶ 3.0.3
```

Check executable paths.
```
echo $PATH
▶ /Users/ab-watthajak/.rvm/gems/ruby-2.6.2/bin:/Users/ab-watthajak/.rvm/gems/ruby-2.6.2@global/bin:/Users/ab-watthajak/.rvm/rubies/ruby-2.6.2/bin:/Users/ab-watthajak/.rvm/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

**Upgrade Ruby (Dev) using RVM**

Install `Ruby` dev version to `RVM` list.
```
rvm install ruby-head
```

Set the `Ruby` dev version as a default.
```
rvm use ruby-head --default
```

Check `Ruby` versions on `RVM` list.
```
rvm list rubies
▶    ruby-2.6.2 [ x86_64 ]
  =* ruby-head [ x86_64 ]
  
  # => - current
  # =* - current && default
  #  * - default
```

Check `Ruby` & `Gem` version.
```
ruby -v
▶ ruby 2.7.0dev (2019-03-20 trunk 67314) [x86_64-darwin18]

gem -v
▶ 3.1.0.pre1
```

Check executable paths.
```
echo $PATH
▶ /Users/ab-watthajak/.rvm/gems/ruby-head/bin:/Users/ab-watthajak/.rvm/gems/ruby-head@global/bin:/Users/ab-watthajak/.rvm/rubies/ruby-head/bin:/Users/ab-watthajak/.rvm/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

Check the `Ruby`'s source directory.
```
which ruby
▶ /Users/ab-watthajak/.rvm/rubies/ruby-head/bin/ruby
```
**Uninstall RVM**

Uninstall the `RVM`.
```
rvm implode
```

Remove the `RVM`'s source directory.
```
rm -rf ~/.rvm
```

Remove the `RVM`'s the system file and directory.
```
rm -rf ~/.rvmrc
rm -rf /etc/rvmrc
```

![Optional](/README/images/optional.png) Find and remove the `RVM`'s aliases inside `.bashrc`.
```diff
- # Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
- [[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm" # Load RVM function
```

![Optional](/README/images/optional.png) Find and remove the `RVM`'s aliases inside `.bash_profile`.
```diff
[[ -s "$HOME/.profile" ]] && source "$HOME/.profile" # Load the default .profile

- source /Users/macbookprogomin/.rvm/scripts/rvm
```

![Optional](/README/images/optional.png) Find and remove the `RVM`'s aliases inside `.profile`.

```diff
- # Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
- export PATH="$PATH:$HOME/.rvm/bin"

- [[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm" # Load RVM into a shell session *as a function*
```

![Optional](/README/images/optional.png) Find and remove the `RVM`'s aliases inside `.zshrc`.

```diff
- # Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
- [[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm"
```

Check executable paths after restart the iTerm.
```
echo $PATH
▶ /usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

### 1.3 RubyGems & Install Rails.

**RubyGems.**

![RubyGems](/README/images/1-3-rubygems-logo.png)

Check the `Gem` version.
```
gem -v
▶ 3.1.0.pre1
```

Update the `Gem` version.
```
gem update --system
▶ Latest version already installed. Done.
```

Display the gem dependencies on your computer.
```
gem list
```


Update the gem dependencies.
```
gem update
```

Find and remove the old gem dependencies.
```
gem cleanup
```
**Install Rails.**

![Rails](/README/images/1-3-rails-logo.png)

Install the `Rails` using the `Gem`.
```
gem install rails -v 6.0.0.beta3
```

Make sure the `Rails` has been installed<br>
by checking the `Rails`'s version.
```
rails -v
▶ Rails 6.0.0.beta3
```
**Uninstall Rails.**

Completely uninstall `Rails`.
```
gem uninstall rails -v 6.0.0.beta3
gem uninstall railties -v 6.0.0.beta3
```

### 1.4 Install Yarn.

![RubyGems](/README/images/1-4-yarn-logo.png)

Install the Yarn on Mac using the `Homebrew`.
```
brew install yarn
```

Check the `Yarn`'s version.
```
yarn -v
▶ 1.15.2
```

### 1.5 Generate a Rails application with Webpacker + React.

Create a new directory. 
```
mkdir react-on-rails
```
`react-on-rails` is the directory's name.

Open the directory.
```
cd react-on-rails
```

Generate a Rails application inside the directory.
```
rails new . --webpack=react
```

![Generate a Rails application with Webpacker + React](/README/images/1-5-generate-a-rails-application-with-webpacker-react.gif)

![Tree Logo](/README/images/1-5-tree-logo.png)

![Optional](/README/images/optional.png) Install tree on Mac using the `Homebrew`.
```
brew install tree
```

![Optional](/README/images/optional.png) Display the repository's tree directory.
```
tree -L 1
▶ .
  ├── Gemfile
  ├── Gemfile.lock
  ├── README.md
  ├── Rakefile
  ├── app
  ├── babel.config.js
  ├── bin
  ├── config
  ├── config.ru
  ├── db
  ├── lib
  ├── log
  ├── node_modules
  ├── package.json
  ├── postcss.config.js
  ├── public
  ├── storage
  ├── test
  ├── tmp
  ├── vendor
  └── yarn.lock
```

Start the Rails's server.
```
bundle exec rails s
```

Display the application on a web browser using the url below.
```
http://localhost:3000/
```

![Start the Rails's server](/README/images/1-5-start-the-rails-server.gif)

### 1.6 Setup Docker.

![Setup Docker](/README/images/1-6-setup-docker.png)

**Install Docker.**

![Docker](/README/images/1-6-docker-logo.png)

Install the `Docker` on Mac using the `Homebrew`.
```bash
brew install docker
```

Check the `Docker` version.
```bash
docker -v
▶ Docker version 18.09.4, build d14af54
```
**Install VirtualBox.**

![VirtualBox](/README/images/1-6-virtualbox-logo.png)

Install the `VirtualBox` on Mac using the `Homebrew`.
```bash
brew cask install virtualbox
▶ 🍺  virtualbox was successfully installed!
```

Check the `VirtualBox` version.
```bash
vboxmanage --version
▶ 6.0.4r128413
```
**Install Docker Machine.**

![Docker](/README/images/1-6-docker-machine-logo.png)

Install the `Docker Machine` on Mac using the `Homebrew`.
```bash
brew install docker-machine
```

Check the `Docker Machine` version.
```bash
docker-machine -v
▶ docker-machine version 0.16.1, build cce350d
```
**Setup Docker Machine.**

Create a default Docker Machine.
```bash
docker-machine create default
```

![Optional](/README/images/optional.png) Check available `virtual machine` list.
```bash
vboxmanage list vms
▶ "default" {eddc73af-e6cf-41bc-b67e-7c9c9f6cdaad}
```

![Optional](/README/images/optional.png) Check running `virtual machine` list.
```bash
vboxmanage list runningvms
▶
```
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
**Connect all shell sessions to Docker Machine.**

Open the `zshrc` config file using the `Vim` editor.
```bash
vi ~/.zshrc
```

| Command | Description |
| --- | --- |
| i | Insert mode. |
| esc | Exit Insert mode. |
| :wd | Save and Exit. |

More about [VIM Editor Commands](https://www.radford.edu/~mhtay/CPSC120/VIM_Editor_Commands.htm).

Add the Docker Machine shell connection command inside `.zshrc`.
```diff
+ eval "$(docker-machine env default)"
```

![Connect all shell session to Docker Machine](/README/images/1-6-connect-all-shell-session-to-docker-machine.gif)
<br>
<br>
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
**Install Python Package Manager.**

![Docker](/README/images/1-6-python-package-manager-logo.png)

```bash
brew install python
```

```bash
python3 --version
▶ Python 3.7.2
```

```bash
pip3 --version
▶ pip 19.0.2 from /usr/local/lib/python3.7/site-packages/pip (python 3.7)
```
**Install Docker Compose.**

![Docker](/README/images/1-6-docker-compose-logo.png)

Install the `Docker Compose` on Mac using the `Python Package Manager`.
```bash
pip3 install docker-compose
```

Check the `Docker Compose` version.
```bash
docker-compose -v
▶ docker-compose version 1.23.2, build 1110ad0
```
