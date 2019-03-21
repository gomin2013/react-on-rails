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
