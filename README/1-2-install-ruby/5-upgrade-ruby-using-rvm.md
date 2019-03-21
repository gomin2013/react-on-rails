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
