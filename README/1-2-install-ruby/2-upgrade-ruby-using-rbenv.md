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
