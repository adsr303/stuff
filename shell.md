# Linux shell fun

Browse POSIX manpages:

```sh
whatis -s 1posix -w '*' | sed 's/ (1posix)//' |
  fzf --preview='echo {} | cut -f 1 | xargs -l man 1posix 2>/dev/null'
```
