---
id: terminal-basics
title: Basic command line tools for unix terminal
sidebar_label: Terminal Basics
---

## Linux Basic Commands

- `pwd` : prints working directory.

- `ls` :lists all the folders in current directory (This will list only visible files and folders (hidden files will not be visible)

- `ls-al` : list all the folders and files which includes hidden files with permissions like r- read w-write x- execute

- `ls -a` Document/  : `-a` is flag, `Document/` is argumemnts

- `.` : current folder, `..` : prev folder

- `cd folder/`

- `cd ..`

- `cd ~` : current home director

- `history` :list out all the command lines we used

- `clear` : to clear the shell

- `volumes`, mount- external drives pendrive etc

- `rwx-` read write execute- permissions and gives users who have access to the folder

- `top`- network monitor

- `mkdir`: used to create new directory
- `mkdir folderName/` : mkdir followed by folder name
- `cd fol(TAB)`- auto complete
- `touch helloworld.sh`: create new file

## Vi Basics

- `vi hellowrod.sh` :create new files
- `./helloworld.sh` : to execute the current directory file 
- `vi`- only keyboard not mouse- Visual only mode
- `hjkl`- navigate like arrow top bottom right left
- `i`: insert mode to start typing text in vi
- `ESC` - to escapte from insert
- `:` enter command mode
- `:w` - write (Save mode)
- `:q` - quit
- `:wq` - write and quit (save and close)

## Permission Basics

- `chmod` - modify the current use permission
- `cdmod +x helloworld.sh` : +x modified the user to have execute access
- `cdmod -x helloworld.sh` : -x removes the execute access

[Link to File Permissions Tutorial](https://www.filepermissions.com)

All the system commands are softwares in linux
- which ls : outputs : /usr/bin/ls - ls is a software
- echo $Path
    lists all the paths the os will search when looking for a command
- cat helloworld.sh - view the content of the file 

## Package Managers:
Package managers helps to download and install the packages and its dependencies. which reduces manual work of configuration
lock: has all the manuals logged what packages are installed including dependecies - u can view and remove if u want
ubundu apt install and remove
feroro: yum install and remove
windows: has chocolaty package manager- need to try
mac has brew cask as package manager

- rm : delete
- rm -r fooldername/ : deletes the folder (-r is flag)


- `mkdocs: ZEN KNOWLEDGE BASE`
- `pip install mkdocs`