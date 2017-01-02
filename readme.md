# oneline

One liner commands.

## Zsh

List directories that are not managed by git.

```
for i in $(ls -1); do if ls -l "$i"/.git > /dev/null 2>&1; then ; else echo "$i"; fi; done
```
