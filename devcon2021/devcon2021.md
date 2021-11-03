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
- telegraph: 5 needle telegraph, telegraph key, operators
- typewriters: hansen writing ball, index typewriter, sholes & glidden
- teleprinter: baudot keyboard, teletype model 33, creed model 7
- computer terminals: datapoint 3300, ibm 2250, vt100, adm-3a
- terminal emulators: kitty, terminator, alacritty, xterm

# command line history
- multics: abandoned operating system because of complexity
- unix: much simpler

> this is the unix philosophy: write programs that do one thing and do it well.
> write programs to work together. write programs to handle text streams, because
> that is a universal interface.
>
> -- douglas mcilroy

# the shell
- v6: shell on version 6 of unix
- sh: bourne shell
- bash: gnu bourne-again shell
- zsh: the z shell
- fish: the friendly interactive shell
- nu: a new type of shell

# basic navigation
- pwd: print working directory
- cd: change working directory
- ls: list directory contents
- find: search for files in a directory
- fd: modern alternative to find

# file manipulation
- touch: change file timestamps
- cp: copy files
- mv: move/rename files
- rm: remove files

# the unix pipe
- echo: display text
- `>`: redirect stdout to a file
- cat: concatenate files to standard output
- `<`: redirect file contents to stdin
- `|`: redirect stdout to stdin for another command
- `$()`: redirect stdout to be a commandline argument
- yes: output a string repeatedly until killed
- head: output the first part of a text stream
- tail: output the last part of a text stream

# filtering, sorting, & aggregating
- grep: print lines that match patterns
- rg: modern alternative to grep
- sort: sort lines of text
- uniq: print or omit duplicated lines
- wc: print newline, word, and byte counts for text
- fzf: commandline fuzzy finder

```
(echo hi && yes hello) | head -n 10 | uniq -c | awk '{print $1 " " $2}'
```

# executables
- chmod: change file access permissions
- file: determine file type
- which: locate program in path
- `$PATH`, `#!/bin/bash`, `#!/bin/python3`, `#!/bin/perl`...

```
$(echo $PATH | tr : ' ' | xargs fd . --exact-depth 1 2>/dev/null | fzf)
```

# cli editors
- ed: line oriented text editor
- ex & vi: full screen text editor
- vim: vi improved
- nvim: modern version of vim
- kak: a spinoff of vim
- helix: a spinoff of kak written in rust
- nano: easy to use editor
- emacs: a very extensible editor
- spacemacs & doom emacs: vim friendly extensions to emacs

# multiplexing
- screen: terminal multiplexer
- tmux: newer terminal multiplexer
- byobu: screen & tmux defaults
- zellij: rust based terminal workspace

similar to gui-based tiling window managers (bspwm, i3, awesome, sway, amethyst, yabai).

# documentation
- man: format and display manual pages
- info: read info documents
- tldr: display simple help pages
- navi: interactive cheat sheet tool
- cheat: minimalistic cheat sheets

# fun exercises
```sh
tldr -l | tr "'" '"' | jq .[] -r | fzf | xargs tldr
```

# philosophy more?
in school, i was told to never 
couldn't tell you who said never do this, but i do remember hearing that.
it's like saying you can't depend on a webservice, because it's not in the same internet as your webservice.

```cpp
// g++ -x c++ -
#include <iostream>

int main() {
    std::system("echo 👋🌍");
    return 0;
}
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
