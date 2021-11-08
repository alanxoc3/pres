---
title: the command line
author: alan morgan
---

# whoami
alan morgan:
- software engineer at clearwater analytics.
- linux user for 10 years.
- obsessed with the command line.

```end-script
./pres title
```

# terminal & command line history
- 1908: first teleprinter
- 1948: first modern computer
- 1964: first computer terminal
- 1969: work on unix begins
- 1975: unix is distributed outside bell labs
- 1976: first computer terminals with movable cursor
- 1991: work on linux begins
- 1999: mac os is now unix based

# the shell
- sh: bourne shell
- bash: gnu bourne-again shell
- zsh: the z shell
- fish: the friendly interactive shell

# basic navigation
- exit: leave a shell or ctrl-d
- clear: clear the screen or ctrl-l
- pwd: print working directory
- cd: change working directory
- ls: list directory contents
- mkdir, touch, cp, mv, rm, rmdir

# viewing files
- cat: concatenate to standard output
- head: print the first part of files
- tail: print the last part of files
- less: interface to view long output

# the unix pipe
- echo: print something
- `>`: redirect stdout to a file
- `|`: redirect stdout to stdin for another command
- grep: filter lines

# unix pipe exercise
try to print the most common word of a file:

```sh
cat LICENSE | ...
```

# unix pipe solution
here is one solution to print the most common word in a file:

```sh
cat LICENSE
| tr ' ' '\n'
| sed -E 's/\W//g'
| awk '/.+/ {print tolower($0);}'
| sort
| uniq -c
| sort -n
| tail -n 1
| awk '{print $2;}'
```

# files & executables
- file: determine file type
- g++: c compiler
- chmod: change file access permissions
- which: locate program in path

# env variables
- $USER: current user
- $PWD: current working directory
- $HOME: current user's home directory
- $PATH: directories where to look for executables

# multiplexing
similar to gui-based tiling window managers (bspwm, i3, awesome, sway, amethyst, yabai).

- screen: terminal multiplexer
- tmux: newer terminal multiplexer

other multiplexers/frameworks: byobu, zelij

# cli editors
- ed: line oriented text editor
- ex & vi: full screen text editor
- vim: vi improved
- nano: easy to use editor
- emacs: a very extensible editor

# modern editors
- nvim: modern version of vim
- kak: a spinoff of vim
- spacemacs & doom emacs: vim friendly extensions to emacs

# documentation
- dotfiles: a place to manage your configuration & notes
- alias: create an alias of a complex command
- `--help`: common option on commands
- man: format and display manual pages
- info: read info documents
- tldr: documentation before a man page

# modern tooling upgrades
- rg: grep clone but faster
- fd: find clone with better interface
- exa: ls clone with knowledge of git
- bat: cat clone with syntax hilighting

# TODO: fuzzy finding
- fzf: commandline fuzzy finder

fuzzy find all tldr tldr help snippets
```sh
tldr -l | tr "'" '"' | jq .[] -r | fzf | xargs tldr
```

fuzzy find all executables in your path
```sh
echo $PATH | tr : ' ' | xargs fd . --exact-depth 1 2>/dev/null | fzf
```

# 😟 many commands i don't have time for
- mpv, wget, curl, nmap, socat
- pass, ranger, diff-so-fancy
- browsh, w3m, lynx, amfora
- lookatme, asciinema
- irssi, ii
- mutt, himalaya
- and many more...

# references
> this is the unix philosophy: write programs that do one thing and do it well.
> write programs to work together. write programs to handle text streams, because
> that is a universal interface.
>
> -- douglas mcilroy

View this presentation as a markdown file at: [git.io/devcon2021](https://git.io/devcon2021)

Some possibly related links:
- [Unix Philosophy](https://en.wikipedia.org/wiki/Unix_philosophy)
- [Language Discussion](https://www.youtube.com/watch?v=xnCgoEyz31M)
- [Baudot Code](https://en.wikipedia.org/wiki/Baudot_code)
- [Punch Card Programming](https://www.youtube.com/watch?v=KG2M4ttzBnY)
- [Command Line History](https://en.wikipedia.org/wiki/Command-line_interface#History)
- [Silly Command Line Tools](https://opensource.com/article/18/12/linux-toy-boxes)
- https://en.wikipedia.org/wiki/History_of_computing_hardware
- [Cat Ascii Art](https://www.asciiart.eu/animals/cats)
