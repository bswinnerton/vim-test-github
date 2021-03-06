# GitHub Test Runner for vim-test

This is a Vim plugin that adds a test runner to
[vim-test](https://github.com/janko-m/vim-test) specifically for
`github/github`.

This allows your cursor to be inside of a test definition, and it will figure
out the appropriate line number to run.

![screencap](https://cloud.githubusercontent.com/assets/934497/15637842/49047822-25e7-11e6-9347-1c798f89918d.gif)

### Installing

Install `vim-test` and this plugin:

```viml
Plug 'janko-m/vim-test'
Plug 'bswinnerton/vim-test-github'
```

Add the following after the test definition from above:

```viml
let test#runners = {'Ruby': ['GitHub']}
```

### vim-test Configuration

Vim-test supports a [number of
strategies](https://github.com/janko-m/vim-test#strategies) to asynchronously
run tests from Vim. I like [vimux](https://github.com/benmills/vimux), to use it
you can set the following in your `~/.vimrc`:

```viml
let test#strategy = "vimux"
```

I'd also recommend making it easy to run vim-test from a key sequence:

```viml
nmap <silent> <leader>t :TestNearest<CR>
nmap <silent> <leader>T :TestFile<CR>
nmap <silent> <leader>a :TestSuite<CR>
nmap <silent> <leader>l :TestLast<CR>
```

### Known Issues

- Currently there is only support for minitest "spec" syntax
