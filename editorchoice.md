# Choosing a text editor for coding

You need a tool that allows you to efficiently edit code.
Such an editor should have the following features:

* Recognize which programming language you are using from the file name.
  For example, `Python` files end with `.py`, and the editor should recognize that.
* Highlight your code.
  This means that keywords, variables, etc., will show up in color and maybe bold or italic face.
  This coloring makes code much more readable.
* Have reasonable auto-formatting of your code.
* Be configurable with respect to how code is formatted.
* Work well with external tools such as `git` and tools to check code for correctness as you edit.
* It is nice to be able to edit local files as well as those on remote servers.

## Editor or IDE?

An editor is a "lighter" application than an "Integrated Development Environment", or `IDE`.
The latter may bundle compilers, debuggers, and other tools.
An editor simply edits text, although many editors allow other tools to be run via interactions with the system.
Many widely-used "programmer's" editors blur the lines between editor and `IDE` because they can be heavily configured to do a lot of the "`IDE` stuff".

## So, which editor?

I will not recommend a specific editor.
There is a long history of pointless "editor wars" where features are compared and one editor is declared supreme.
Lots of good editors exist.
Pick one.
Learn how to use it.
Then learn how to use it *well*, meaning that you can configure it to make your work more streamlined and faster.

The only wrong choices are:

* Word processors.
* Anything that cannot be reconfigured to input a specific number of spaces when the `tab` key is hit.

### vim and emacs

The most widely-known and used open-source editors in this category are [vim](https://www.vim.org) and [GNU Emacs](https://www.gnu.org/software/emacs/).
Either of these is an excellent choice.
They work very differently from each other.
`vim` is especially "out there" in its interface with respect to pretty much any other editor.
(But there is definitely a method to `vim`'s madness.)

When it comes to editing remote files and syntax highlighting, `emacs` is incredibly good.

The plugin ecosystem for `vim` is incredible.
The plugins allow all sorts of new commands specific to the file types that you are working on.
(`Emacs` has this, too, but I find it easier to get into with `vim`.)

The user communities for both editors are basically maniacal cults.

### List of editors

You may consider any of the following:

* [GNU Emacs](https://www.gnu.org/software/emacs/)
* [vim](https://www.vim.org)
* [neovim](https://neovim.io)
* [atom](https://atom.io/)
* Microsoft's [VS code](https://code.visualstudio.com/)

I am not including anything that is specific to a single operating system.
The above list is incomplete.
If you already use something else, or find something else that meets your needs, then go for it.

Honorable mention goes to [GNU nano](https://www.nano-editor.org/).
While `nano` is easy to use, it seems to fall short compared to the editors listed above.

## What KT does

I used `emacs` for 15-20 years.
Eventually, the key combinations started to cause ergonomic issues for me.
As a result, I now use [neovim](https://neovim.io), which is a fork of `vim`.
The `vim` interface requires much less in the way of hand/wrist movement, which has helped manage pain from typing.
`neovim` has the same or similar feature set as `vim` 8.1.
The main difference that most users see is that `neovim` sets a lot of very nice defaults.

My `neovim` configuration can be found [here](https://github.com/molpopgen/dotfiles).

