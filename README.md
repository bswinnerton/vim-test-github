# GitHub strategy for vim-test

This is a Vim plugin that adds a strategy to
[vim-test](https://github.com/janko-m/vim-test) specifically for
`github/github`.

This allows your cursor to be inside of a test definition, and it will figure
out the appropriate line number to run.

### Installing

Install `vim-test` and the plugin:

```vimscript
Plug 'janko-m/vim-test'
Plug 'bswinnerton/vim-test-github'
```

Add the following below the plugin definitions from above:

```vimscript
let test#runners = {'Ruby': ['GitHub']}
```
