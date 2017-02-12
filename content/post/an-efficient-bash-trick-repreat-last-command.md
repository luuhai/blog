+++
date = "2017-02-12T23:42:32+07:00"
title = "An efficient bash trick: repeat last command"
draft = false

+++

If you want to repeat the last command, just type in `!!`

```bash
$  echo blah
blah
$  !!
echo blah
blah
```

The most common use of this trick is to prepend `sudo` to the command

```bash
$  pacman -S go
error: you cannot perform this operation unless you are root.
$  sudo !!
sudo pacman -S go
[sudo] password for root:
```

What if you only want to repeat the last command's arguments? Use `!*` instead of `!!`

```bash
$  la ~/.config/i3/
bash: la: command not found
$  ls !*
ls ~/.config/i3/
config
```
