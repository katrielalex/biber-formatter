# biber-formatter

[pre-commit](pre-commit.com) hook to check or autoformat your biber files for you.

## Installing

Add

```
-   repo: git://github.com/katrielalex/biber-formatter
    sha: v1
    hooks:
    -   id: biber-autoformat
```

to your `.pre-commit-config.yaml`. You can use `biber-check-format` if you don't want to modify files and just want to get a warning about them.

_Beware_: biber doesn't like newlines at the end of files, so if you have the `end-of-file-fixer` hook enabled you should make sure to have it skip your `.bib` files, like this:

```
    -   id: end-of-file-fixer
        exclude: '\.bib$'
```
