# load-bash-shell-aliases

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

Convert bash aliases into eshell ones.

## Installation

1. Download and copy **load-bash-shell-aliases.el** into
   **.emacs.d/lisp** directory.
2. Add the following elisp code to your Emacs config:

``` elisp
;; Tell Emacs where is your personal elisp lib directory
(add-to-list 'load-path "~/.emacs.d/lisp/")

;; load-bash-shell-aliases
;; https://github.com/daviderestivo/load-bash-shell-aliases
(load-library "load-bash-shell-aliases")
```

3. Call lbsa/load-bash-alias-into-eshell interactive function to
   convert bash aliases into eshell ones:

```
M-x lbsa/load-bash-alias-into-eshell
```

## Customization

The location of your barshrc file can be customized by setting the
value of **lbsa/bashrc-file** variable:

``` elisp
(setq lbsa/bashrc-file "~/.bashrc")
```

In addition it's possible to exclude certain bash aliases to be converted into eshell ones simply setting **lbsa/exclude-aliases-regexp**:

``` elisp
(setq lbsa/exclude-aliases-regexp "^alias magit\\|^alias oc")
```

## Credits
The original ideas for this package has been taken from [Skye](http://skyefreeman.io/programming/emacs/2017/08/03/converting_bash_config_to_eshell.html). The original elisp code can be found [here](https://github.com/skyefreeman/.emacs.d/blob/master/custom/bash-to-eshell-aliases.el).
