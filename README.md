# tsx-mode.el: a batteries-included major mode for TSX/JSX files

use lsp-mode for code analysis and completion, tree-sitter for highlighting and indentation, and some godawful hacks for CSS-in-JS support.  Aims to provide proper JSX/TSX indentation and syntax highlighting as well as some fancy features related to CSS-in-JS.

Screenshot:

![](https://repository-images.githubusercontent.com/461083728/1bc1d312-661c-40b9-abda-97c8e7f9e4b2)

## Installation

0. Dependencies:
Emacs 28.1+ with the following packages installed:
 - [`tree-sitter`](https://emacs-tree-sitter.github.io/installation/)
 - [`tsi.el`](https://github.com/orzechowskid/tsi.el)
 - [`lsp-mode`](https://github.com/emacs-lsp/lsp-mode)
 - [`company`](https://github.com/company-mode/company-mode)
 - [`origami.el`](https://github.com/gregsexton/origami.el)
1. Install: download this package and place `tsx-mode.el` inside a directory on your `load-path`.
  
> or install this repository (and all its package dependencies) via `straight.el`: `(straight-use-package '(tsx-mode :type git :host github :repo "orzechowskid/tsx-mode.el"))`
2. Require: `(require 'tsx-mode)`
3. Enable: `(tsx-mode t)`

## Keybindings

all tsx-mode keybindings live under the `C-c t` prefix.

| Binding   | Command                                          | Function                       |
| --        | --                                               | ---                            |
| `C-c t f` | toggle code-folding for current CSS-in-JS region | `tsx-mode-css-toggle-fold`     |
| `C-c t F` | toggle code-folding for all CSS-in-JS regions    | `tsx-mode-css-toggle-fold-all` |

## Configuration

Useful variables are members of the `tsx-mode` customization group and can be viewed and modified with the command `M-x customize-group [RET] tsx-mode [RET]`.

## Bugs and limitations

tons!

- lsp-mode is currently the only supported LSP client.
- TS/TSX indentation might not be quite right.  (if you notice something, please open an issue against [tsi.el](https://github.com/orzechowskid/tsi.el))
- CSS indentation might not be quite right either.  (if you notice something, please open an issue against this repo)
- only a couple of CSS-in-JS formats are currently supported.

## License

GPLv3.  see LICENSE in the top level of this repository.
