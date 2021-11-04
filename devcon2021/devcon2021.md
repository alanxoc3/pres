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

# terminal emulator history
- telegraph: morse code, baudot code
- typewriters: sholes & glidden
- teleprinter: teletype model 33, creed model 7
- computer terminals: datapoint 3300, ibm 2250, vt100, adm-3a
- terminal emulators: kitty, terminator, alacritty, xterm

# command line history
- 1964: work on multics begins
- 1969: work on unix begins
- 1975: unix is distributed outside bell labs
- 1991: work on linux begins
- 1999: mac os is now unix based

> this is the unix philosophy: write programs that do one thing and do it well.
> write programs to work together. write programs to handle text streams, because
> that is a universal interface.
>
> -- douglas mcilroy

# the shell
- sh: bourne shell
- bash: gnu bourne-again shell
- zsh: the z shell
- fish: the friendly interactive shell
- exit: leave a shell or ctrl-d
- clear: clear the screen or ctrl-l or reset

# basic navigation
- pwd: print working directory
- cd: change working directory
- ls: list directory contents
- find: search for files in a directory

# file manipulation
- mkdir: create a directory
- touch: change file timestamps
- cp: copy files
- mv: move/rename files
- rm: remove files
- rmdir: remove a directory

# files & executables
- cat: concatenate files to standard output
- file: determine file type
- chmod: change file access permissions
- which: locate program in path

# env variables
- echo: print something
- $USER: current user
- $PWD: current working directory
- $HOME: current user's home directory
- $PATH: directories where to look for executables
- env: list all env vars

# the unix pipe
- `>`: redirect stdout to a file
- `|`: redirect stdout to stdin for another command
- head: output the first part of a text stream
- tail: output the last part of a text stream
- less: interface to view long output
- wc: print newline, word, and byte counts for text

# unix pipe example
try to print the word that is most common in a file

```sh
cat LICENSE | ...
```

# cli editors
- ed: line oriented text editor
- ex & vi: full screen text editor
- vim: vi improved
- nano: easy to use editor
- emacs: a very extensible editor

# documentation
- man: format and display manual pages
- info: read info documents
- `--help`: common option on commands

# multiplexing
- screen: terminal multiplexer
- tmux: newer terminal multiplexer
- byobu: screen & tmux defaults
- zellij: rust based terminal workspace

similar to gui-based tiling window managers (bspwm, i3, awesome, sway, amethyst, yabai).

# modern tooling upgrades
- rg: grep clone but faster
- fd: find clone with better interface
- exa: ls clone with knowledge of git
- bat: cat clone with syntax hilighting
- tldr: documentation before a man page

# modern editors
- nvim: modern version of vim
- kak: a spinoff of vim
- spacemacs & doom emacs: vim friendly extensions to emacs

# fuzzy finding
- fzf: commandline fuzzy finder

# fzf examples
fuzzy find all tldr tldr help snippets
```sh
tldr -l
| tr "'" '"'
| jq .[] -r
| fzf
| xargs tldr
```

# fzf path
fuzzy find all executables in your path
```sh
$(echo $PATH | tr : ' ' | xargs fd . --exact-depth 1 2>/dev/null | fzf)
```

# more topics that i won't get into
- docker, hugo, nmap, socat, group management, ...
- don't be afraid to look in random directories on your computer. you might learn something.
- must have: fzf! show example usage for fzf.
- pass, fzf, fd, rg, ranger, diff-so-fancy, nvim, kak, w3m, lynx, irssi, lam, asciinema
- docker run --rm -it browsh/browsh
- gemini/gopher
- w3m, lynx, browsh
- irssi - irc
- himalaya/mutt - email

# references
View this presentation as a markdown file at: [git.io/devcon2021](https://git.io/devcon2021)

- [Unix Philosophy](https://en.wikipedia.org/wiki/Unix_philosophy)
- [Language Discussion](https://www.youtube.com/watch?v=xnCgoEyz31M)
- [Baudot Code](https://en.wikipedia.org/wiki/Baudot_code)
- [Punch Card Programming](https://www.youtube.com/watch?v=KG2M4ttzBnY)
- [Command Line History](https://en.wikipedia.org/wiki/Command-line_interface#History)
- [Silly Command Line Tools](https://opensource.com/article/18/12/linux-toy-boxes)

https://xoc3.io/2021-11-17
