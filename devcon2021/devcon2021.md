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

# history of command line hardware
- 1908: first teleprinter
- 1948: first modern computer
- 1964: first computer terminals
- 1976: first computer terminals with movable cursor
- 1979: first guis appear

# history of command line software
- 1961: time sharing is implemented
- 1964: work on multics begins
- 1969: work on unix begins
- 1975: unix is distributed outside bell labs
- 1991: work on linux begins

# the shell
- echo: print text
- sh: bourne shell
- bash: gnu bourne-again shell
- zsh: the z shell
- fish: the friendly interactive shell

# navigation
- exit: leave a shell or ctrl-d
- clear: clear the screen or ctrl-l
- pwd: print working directory
- cd: change working directory
- ls: list directory contents

# cli editors
- ed: line oriented text editor
- vi: full screen text editor
- vim: vi improved
- nano: easy to use editor
- emacs: a very extensible editor
- nvim: modern version of vim
- kak: a spinoff of vim

# unix pipe
- `>`: redirect stdout to a new file
- cat: concatenate to standard output
- `|`: redirect stdout to stdin for another command
- head: print the first part of files
- tail: print the last part of files

# unix pipe exercise
which character is the most common in a file?

```sh
cat x
| sed -E 's/(.)/\1\n/g'
| awk '/\S/{print $1;}'
| sort
| uniq -c
| sort -n
| awk 'END {print $1;}'
```

# documentation
- man: format and display manual pages
- `--help`: common option on commands
- tldr: documentation before a man page
- alias: create an alias of a complex command

# modern tooling upgrades
- exa: ls clone with knowledge of git
- rg: grep clone but faster & better
- fd: find clone but faster & better
- bat: cat clone with syntax hilighting
- fzf: commandline fuzzy finder

# fzf with fd
```sh
fzf_cat_file() {
    cat $(fd -t f | fzf -m)
}
```

```sh
fzf_cd_dir() {
    cd $(fd -t d | fzf)
}
```

# fzf shell history
```sh
fzf_exec_history() {
    $(fc -rl 1 | fzf --nth 2.. | awk '{$1="";print $0;}')
}
```

# fzf emojis
```sh
fzf_emoji() {
    emoji-fzf preview | fzf -m --with-nth 2.. -d ' ' | cut -d ' ' -f 1 | emoji-fzf get
}
```

# fzf with rg and kak
```sh
fzf_rg() {
    RG_LINE=$(rg '' -n --color always | fzf --with-nth 2.. -d ':')
    FILE=$(cut -d ':' -f 1 <<< $RG_LINE)
    LINE=$(cut -d ':' -f 2 <<< $RG_LINE)
    [[ -n "$FILE" ]] && kak +$LINE $FILE
}
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
