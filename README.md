# bashrc_notify
- Do you ever execute commands that take a long time to finish?
- Do you ever start doing something else and forget about the command?
- Do you ever notice you've spent too long doing something else?
Worry not!

## Notify after execution
Add the following in your `~/.bashrc`
```sh
notify() {
    paplay /path/to/your/favorite/sound/file
}
```

load your new configuration with:
```sh
$ source ~/.bashrc
```

and use it like so:
```sh
$ some_commmand_that_takes_forever && another_command && notify
```

Your favorite sound will play when the commands have finished!

## What about failed commands?
If you want to hear whether your command(s) executed successfully or failed, you can do the following:
```sh
$ some_command_that_takes_forever && paplay <path/to/success/sound> || paplay <path/to/failure/sound>
```

Happy idling!
