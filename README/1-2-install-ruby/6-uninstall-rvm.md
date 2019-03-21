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
