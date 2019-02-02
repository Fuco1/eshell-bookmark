# eshell-bookmark

Simple package integrating eshell with bookmark.el.

Read the [blog post](https://fuco1.github.io/2017-10-08-Using-bookmarks-with-eshell-and-docker-tramp.html) for introduction.

# Installation

Get it from MELPA or MELPA Stable with `M-x package-install eshell-bookmark`.

# Usage

Enable the bookmark by adding this setup to your config:

``` emacs-lisp
(add-hook 'eshell-mode-hook 'eshell-bookmark-setup)
```

Or you can also manually call `(eshell-bookmark-setup)` from any other setup hook you already have.

If you use `use-package`, the setup can look something like the following:

``` emacs-lisp
(use-package eshell-bookmark
  :after eshell
  :config
  (add-hook 'eshell-mode-hook #'eshell-bookmark-setup))
```

After this, use the bookmark features as usual:

* capture a bookmark to eshell with `C-x r m`
* restore an eshell with `C-x r l`

Works with remote/TRAMP hosts as well, which is super cool.
