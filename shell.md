# Linux shell fun

Browse manpages with preview:

```sh
whatis -w '*' | fzf --preview='xargs -I {} -l man {1}{2} 2>/dev/null'
```
