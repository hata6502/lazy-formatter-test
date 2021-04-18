# lazy-formatter-test

A test repository for lazy-formatter.

## Format files

```bash
# prettier.js is formatted by Prettier
# standard.js is formatted by Standard
lazy-formatter write prettier.js standard.js
```

## Check if files are formatted

```bash
$ lazy-format check prettier.js standard.js
# If prettier.js is not formatted
prettier.js should be formatted by: npx prettier --write
# If standard.js is not formatted
standard.js should be formatted by: npx standard --fix
```

This is used in the [CI](), Please see [this Pull Request]().

## Lazy formatter migration

When pushed to `main` branch, the changed files are formatted by Prettier.
By implementing it in [CI](), your project can be lazyly migrated to Prettier.

Please see [this commit]().

## Config

Please see [lazy-formatter.json](https://github.com/hata6502/lazy-formatter-test/blob/main/lazy-formatter.json).
