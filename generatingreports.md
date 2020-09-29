# Tools for generating reports

## Recommendation

KT strongly recommends using `R` markdown over `Jupyter` notebooks.

### Rationale

The main reasons for this recommendation are:

* Works easily with both `R` and `Python`.
* `git`-friendly.
* Does not require a browser.
* Can be edited in a good text editor instead of `RStudio`.
* Easier to convert to other formats, especially manuscripts for submission.

### But Jupyter is fine, too!

As always, there are exceptions to this rule!
KT likes `Jupyter` notebooks, and they are the best/only game in town for generating interactive `Python` graphics.

## R Markdown (and R Studio)

[R Markdown](https://rmarkdown.rstudio.com/) is a "flavor" of `markdown`.
The way most people use `R markdown` is within [RStudio](https://rstudio.com).
`Rstudio` is an "integrated development environment", or `IDE` for the `R` programming language.
It differs from "vanilla" `markdown` is that you can execute `R` code display graphics generated via `R`.
With the [reticulate](https://rstudio.github.io/reticulate/) package installed, you may also do the same with `Python` code.

More info on `R markdown` can be found in the section `Generating content with R markdown` on the [main page](index).

### Pros

* An `R markdown` document is plain text, making it `git`-friendly.
* As it is a plain text format, you can use whatever editor you like.
* Works with both `R` and `Python`
* Can generate various output formats, including `HTML` and `PDF`.
* `RStudio` makes a nice "one stop shop" for a project using `R`.
* `RStudio` has `git` integration!
* The `R markdown` format can be the basis of slides, manuscripts, or books.

### Cons

* Different "flavors" of `R markdown` used for slides, books, etc., can have subtly different ways of doing specific things.
* Documents are compiled from `markdown` to the output format from top to bottom.
  Thus, it can take some time to reprocess a large document.
* `RStudio` is not straightforward to set up for remote work.

## Jupyter Lab

[Jupyter lab](https://jupyter.org/) is a browser-based notebook application that supports many different languages, including `R` and `Python`.
Its language agnosticism means that it is not an `IDE` for any language.
Rather, it is a nice application for entering text and code and making reports, slides, etc..

### Pros

* Works with both `R` and `Python`
* Can generate various output formats, including `HTML` and `PDF`.
* Individual code "cells" can be executed in isolation, so you don't necessarily have to reprocess the entire document.
* Can make very nice slides!

### Cons

* The notebooks are binary files.
  Thus, it is nearly impossible to see the differences between changes using `git`/`GitHub`.
  There are workarounds for this problem, but they aren't as good as plain text.
* Inconvenient for generating output in the right format to submit as a manuscript for publication.
* The browser requirement makes it difficult to use remotely. See [here](http://www.molpopgen.org/coding/tips).
