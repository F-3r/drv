# DragonRuby Version Manager

Minimal DragonRuby Version Manager for Linux written in Bash

## Why?

This small helper has 3 objectives:

1) let you have a single DragonRuby installation per version 
2) let you switch between versions with ease.
3) help structuring your projects so that they are easy to commit into Git (or any other CVS) without leaking DragonRuby files

## How to?

#### Install `drv`

To install the command run:

```bash
wget -O $HOME/bin/drv https://raw.github.com/f-3r/drv/main/drv
```

(Or, alternatively, download the script from that url and save it in a dir listed in your `PATH`)

_note: ensure the file is executable (`chmod +x drv`)_

#### Install a DragonRuby version

* Download a version DragonRuby from https://dragonruby.itch.io/dragonruby-gtk
* unzip it 
* copy the absolute path to the directory where it was extracted
* run `drv install path-you-just-copied`

#### Use it!

Go to a project directory and set the version you want to run it with:

`drv set 4.8` 

This will create a hidden `.drv` file in the project which will store the version (which you can commit into your Git repo)

#### Run the game

To run the game using the set version, run:

`drv run`

And that's basically all there's to it

## Command reference

It has 4 commands:

* **drv versions** => list all installed versions
* **drv set <version>** => activates `<version>` for the current project (current directory)
* **drv run [path-to-game-dir]** => runs the game using the version set for that dir. If no dir provided it will use the current directory
* **drv install <dir>** => Adds the DragonRuby version to the list of available versions

## Contributing
Questions? Issues? Ideas? get in touch!

