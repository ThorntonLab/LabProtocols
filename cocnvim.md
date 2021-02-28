# Setting up coc.nvim

This document describes how to set up [coc-nvim](https://github.com/neoclide/coc.nvim) for `neovim` or `vim`.
For `vim`, you need version 8 or later.

`coc-vim` is a code-completion and linting system.
It works via a language server model similar to Microsoft's VScode.

## Installing the plugin

In your `init.vim` (or `.vimrc`) using [vim-plug](https://github.com/junegunn/vim-plug): 

```
Plug 'neoclide/coc.nvim', {'branch': 'release'}
```

Then, restart `vim` and `:PlugInstall`.

For other plugin managers, do what's needed.

## Installing specific language servers

### C and C++

```
:CocInstall coc-clangd
```

#### Generating compile commands

C and C++ error checking and code completion depends on a file called `compile_commands.json`, which is processed by `clangd`.

First, make sure `clangd` is installed:

```sh
sudo apt install clangd
```

For projects using `cmake`:

```sh
mkdir ccommands
cd ccommands
cmake .. -DCMAKE_EXPORT_COMPILE_COMMANDS=1
mv compile_commands.json ..
cd ..
rm -rf ccomands
```

`meson` generates the file automatically:

```sh
meson build
mv build/compile_commands.json .
```

If using `autotools`:

```sh
sudo apt install bear
```

Then,

```
bear make
```

### Python

```
:CocInstall coc-pyright
```

This section probably needs further updating on configuration.
By default, you get a lot of lint issues flagged, some of which are not necessarily anything to worry about.

### rust

```
:CocInstall coc-rls
```
