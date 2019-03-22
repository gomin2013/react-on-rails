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
