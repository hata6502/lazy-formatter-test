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

This is used in the [CI](https://github.com/hata6502/lazy-formatter-test/blob/main/.github/workflows/check-format.yml),
Please see [this Pull Request](https://github.com/hata6502/lazy-formatter-test/pull/4).

## Lazy formatter migration

When pushed to `main` branch, the changed files are formatted by Prettier.
By implementing it in [CI](https://github.com/hata6502/lazy-formatter-test/blob/main/.github/workflows/format.yml),
your project can be lazyly migrated from Standard to Prettier.

Please see [this commit](https://github.com/hata6502/lazy-formatter-test/commit/1b2b3e5e637bf3409d4469f7690baf5daad469b8).

NOTE: Pull Requests must be **squash merged**.

## Config

Please see [lazy-formatter.json](https://github.com/hata6502/lazy-formatter-test/blob/main/lazy-formatter.json).
