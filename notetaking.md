# Tools for taking notes

The reality of university work is that you are busy with all sorts of different tasks.
You'll find yourself dropping/pausing projects for various lengths of time.
For example, you may not get much research done one week due to a class for which you are the TA.
You need something that lets you take notes, so that "future you" remembers where you left off.
You'll also want to take notes during group meetings, one-on-one meetings, at conferences, etc..

## Feature to look for

* Notes are shareable somehow
* Cross-referencing between notes
* Nice formatting of code, including images, etc..

## "Cloud" solutions

There are many.
The main advantage is auto-syncing across devices and accessibility from your phone/tablet.
A potential disadvantage may be bugs affecting the security of user data.
For example, one hit [Evernote recently](https://techcrunch.com/2019/04/17/evernote-macos-bug/).

Options include:

* [Roam research](https://roamresearch.com/)
* [Microsoft's One Note](https://www.onenote.com/) (We may have access to this via the institutional 365 account, but I have not checked)
* [Evernote](https://evernote.com/)
* [Google Keep](https://keep.google.com) is a super-lightweight option.

## "Local" solutions

An alternative to cloud-based solutions is to use something that works on files stored locally.
If such files are plain text, then you can use GitHub to sync them across machines.
Many of these tools can be used from your text editor.
For example:

* [vimwiki](https://github.com/vimwiki/vimwiki) for `vim`-like editors
* [Org mode](https://orgmode.org) for `Emacs`-like editors
* A plain collection of `markdown` files

For me, the advantage of these is:

* Being able to take notes without an internet connection
* Version control
* Being able to write down code in my notes and have it be nicely highlighted/formatted
* Rendering mathematics using `LaTeX`

## What KT uses

I use the [vimwiki](https://github.com/vimwiki/vimwiki) plugin.
I have it configured to take notes in `markdown` format.
Using `markdown` means that I lose a few features.
However, I gain the ability to easily render my notes as `PDF` or `HTML` to share with people.
I do this rendering from within [neovim](https://neovim.io) using the [vim plugins](https://github.com/vim-pandoc/vim-pandoc) from the `pandoc` group.
I keep my notes version-controlled using `git` and sync them between machines via a *private* repository.
I use a private repository because I keep notes on things like student committee meetings, etc., that should not be public.

When I need a "cloud" service for notes, I use [Google Keep](https://keep.google.com)
