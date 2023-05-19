# DragonRuby Version Manager

Minimal DragonRuby Version Manager for Linux written in Bash

## Why?

This small helper has 3 objectives:

1) let you have a single DragonRuby installation per version
2) let you switch between versions with ease.
3) help structuring your projects so that they are easy to commit into Git (or any other CVS) without leaking DragonRuby files

## How to?

#### Install `drv`

To download and install you only need to put the script somewhere (just remember where), like:

```bash
wget -O $HOME/bin/drv https://raw.github.com/f-3r/drv/main/drv
```
and then source it in you `.bashrc` like:

```bash
echo "source $HOME/bin/drv" >> $HOME/.bashrc
```
and restart your shell.

To check everything's runnning run:

```
drv
```

and you should see the help message

#### Using it

`drv` will automatically detect `.drv` file in the root of you project and set the configured version.

If you set up your projects using `drv setup` that is already taken into account,
so you should be all set and shouldn't need to explicitely run any `drv` command at all

Anyway, here's the list of available commands it supports:

* `drv versions` => list all installed versions
* `drv use <version>` => activates <version>
* `drv install <zip-file>` => installs the DragonRuby version in the zip file
* `drv setup <directory> <version>` => creates a new project skeleton that will use the specified DragonRuby version.

NOTE: you can see the list of commands running `drv` without arguments

#### There's no `run` command! How do I run my game with `drv`?

Well, you don't use `drv` to run your game. You just use the `dragonruby` executable directly
The only thing you need to remember is to pass you game folder as argument, like:

```bash
dragonruby my_game
```

#### How to add a DragonRuby version to `drv`

`drv install` expects a DragonRuby zip, so the steps to install a new version are:

* Download a version DragonRuby from https://dragonruby.itch.io/dragonruby-gtk
* run `drv install path-the-dragonruby-zip-you-just-downloaded`


#### How to change the current DragonRuby version

With the `drv use` command, like: `drv use 4.10`

This will add the DragonRuby installation dir into you PATH env var so your shell can find the correct version of dragonruby.
