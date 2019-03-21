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
