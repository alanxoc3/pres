---
title: the command line
author: alan morgan
---

# who am i?
```beg-script
./pres title
```

alan morgan:
- software engineer at clearwater analytics.
- linux user for 10 years.
- obsessed with the command line.

# history of terminal emulators
- teleprinter/teletype: teletype model 33, creed model 7
- computer terminals: datapoint 3300, ibm 2250, vt100, adm-3a
- terminal emulators: xterm, kitty, alacritty, windows/mac terminal

```end-script
./pres teletype
```

# intro to the unix shell
- shell: sh, bash
- navigation: cd, ls, pwd, find
- management: rm, mv, cp
- viewing: cat, head, tail, less
- filtering: grep
- ...

# the unix philosophy
> this is the unix philosophy: write programs that do one thing and do it well.
> write programs to work together. write programs to handle text streams, because
> that is a universal interface.
>
> douglas mcilroy

douglas mcilroy was the the head of bell labs computer science research and
creator of the unix pipe.

# intro to the modern unix shell
- shell: zsh, fish, nu
- navigation: exa, fd
- management: rsync
- viewing: bat
- filtering: rg, fzf
- ...

# a simplified unix philosophy
write programs that:
- do one thing well
- handle text streams

programs tend to work well with each other if they have only one focus and
handle text streams.

# programs that do one thing well
monolithic architecture vs microservice architecture
why write programs that do one thing well?
- simplicity

# commandline and webservices
unix philosophy is like a microservice architecture. theoretically, the entire
system is composed of simple pieces that work together to achieve something
complex.

# analogies
# do one thing well. like online payment systems to paypal.
# or like other things.
# a brief introduction of the commandline
# managing complexity (man page, tldr...)
# dotfiles
# history of the commandline

# ---
i want to do something on the commandline. what should i do first?
# ---

how about some real world examples?

there
 be many small and simple pieces that work together to make a system
work.

some decent examples
- mv, rm, cat, tee
- cp -> rsync
- ls -> exa

# programs that do one thing well
what can "Finder" or "Windows Explorer" do?

# programs that work well with other programs
# programs that work well with humans

# browsing the file system
- cd, ls, pwd, exit, cat
- ranger
- locate, updatedb, grep
- rg, fzf, fd, exa

# history of cli editors
- ed, em, en, ex, vi: early unix editors some written for teleprinters
- vim, neovim, emacs, kakoune, nano: modern editors

# env vars, shell functions, aliases

# navigating git
- git, diff-so-fancy

# shell built-ins vs utilities
- builtins: exit, cd, 

# important programs in my workflow
- fzf: fuzzy find
- rg: ripgrep

# browsing the web
- gemini/gopher
- w3m, lynx, browsh

# social
- irssi - irc
- himalaya/mutt - email

# hello

https://en.wikipedia.org/wiki/Command-line_interface#History

# what is posix and why should i care?
posix is a standard. we can't have a powerful commandline if no one followed any standard whatsoever. there would be too many incompatible implementations if that was the case.


presenter: alan morgan

Some silly linux CLI things:
https://opensource.com/article/18/12/linux-toy-boxes


what is posi

https://xoc3.io/2021-11-17

in school, i was told to never 
couldn't tell you who said never do this, but i do remember hearing that.
it's like saying you can't depend on a webservice, because it's not in the same internet as your webservice.
```cpp
#include <iostream>

int main() {
    std::system("echo 👋🌍");
    return 0;
}
```

# ideas
- don't be afraid to look in random directories on your computer. you might learn something.
- must have: fzf! show example usage for fzf.

# cheatsheets
tldr:  https://github.com/tldr-pages/tldr
navi:  https://github.com/denisidoro/navi
cheat: https://github.com/cheat/cheat

# references
View this presentation as a markdown file at: [git.io/devcon2021](https://git.io/devcon2021)

- [Unix Philosophy](https://en.wikipedia.org/wiki/Unix_philosophy)

pass, fzf, fd, rg, ranger, diff-so-fancy, nvim, kak, w3m, lynx, irssi, lam, asciinema

docker run --rm -it browsh/browsh

git.io/devcon2021
