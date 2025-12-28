<div align="center">
<h3>todo-ng</h3>
<img src="https://github.com/georgeabr/py-todo-ng/blob/master/todo-ng-1.png">

</div>

## Overview
A little program to remind you of upcoming events / unfinished tasks.  
It uses `json` for storing the appointments.  

Add it to `~/.zshrc` or `~/.bashrc` or whatever you want, and it will stop you from
putting off stuff.


## Dependencies
* python >=3.5 (sys, re, json)

## Tested Platforms
* Linux

* Manual Installation (Linux)
```
$ git clone https://github.com/georgeabr/todo-ng.git
$ cd todo-ng && sudo cp todo-ng /usr/bin/todo-ng
```

## Usage
```
Usage: ./todo-ng <argument>

  a, -a, --add <title> <date or days as YYYY/MM/DD>   -- Add a new item.
                                                      Ex: ./todo-ng -a "Buy milk" 10d
                                                      Ex: ./todo-ng -a "Buy milk" 2025/12/30
  e, -e, --edit <index> <title> <date or days>        -- Edit an item (uses displayed index).
  m, -m, --move <index> <new index>                   -- Move an item (changes disk order).
  r, -r, --remove <indices...>                        -- Remove items (uses displayed index).
  l, -l, --list                                       -- List items.
  h, -h, --help                                       -- Help.
  v, -v, --version                                    -- Version.

Use date in format YYYY/MM/DD - 2020/07/05, or <days>d - 3d, for due date of todo item
Use readline keyboard shortcuts to move around the input buffer

Configuration Options (See ~/.config/todo-ng/config):
color = False
detail_mode = True
week_start_day = Mon
autosort = False

Reminders data file: ~/.local/share/todo-ng/todo.json
```

### Detail Mode

```
  3) Buy CDs                                  # detail_mode = true
    (Due in 2 days, next Tuesday)
  3) Buy CDs                                  # detail_mode = false
    (In 2 days)
```
## Author of the original script, on which this fork is based
Copyright (c) 2017-2018 aesophor
https://github.com/aesophor/py-todo

## License
Available under the [MIT License](https://github.com/georgeabr/todo-ng/blob/master/LICENSE)
