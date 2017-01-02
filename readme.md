# oneline

One line commands (not always one line) that I often forget and rewrite.

### List directories that are not managed by git

```sh
for i in $(ls -1); do if ls -l "$i"/.git > /dev/null 2>&1; then ; else echo "$i"; fi; done
```

### List directories that has dirty git working copy

```
for i in $(ls -1); do if ls -l "$i"/.git > /dev/null 2>&1; then if [ "" = "`cd $i && git status -s`" ]; then; else echo "$i"; fi; fi; done
```

### Run Spring Boot CLI with properties

```
spring run script.groovy -- --server.port=8081
```

## License

MIT &copy; Soichiro Kashima
