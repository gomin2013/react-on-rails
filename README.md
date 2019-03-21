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
