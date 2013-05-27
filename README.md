## Overview

`dired-efap.el` allows the user to edit the filename at point, by hitting a key
(like f2) or double-clicking it. The name is edited in the dired buffer, and the
renaming takes effect when the user hits the RET key. Only the name of the file
at point is tangible and editable, and it uses an special font.

This package provides a similar user interface to renaming files to the
interface used by some graphical file managers (or "explorers", however they are
called).

### Installation

Add `dired-efap.el` to your load-path and this line to your config file:

```lisp
(require 'dired-efap)
(define-key dired-mode-map [f2] 'dired-efap)
```

### Usage

To edit a name you can hit f2 (or the mapping of your choosing) or
double-click over it. Pressing RET the file is actually renamed.  C-g
aborts.

### Customization

The behavior of the mouse can be customized. There are three options:
double-click to edit, click once in the file where the cursor is (this includes
double-click, because the first click moves the cursor) and disallow the use of
the mouse to edit names. See and customize the variable `dired-efap-use-mouse'
to change the default behavior.

You can customize also the face of the name being edited. This face is called
`dired-efap-face`.  Default face inherits from your default face, with a box
around it.

See also variable `dired-efap-initial-filename-selection`, if you want to
control what part of the filename will be initially selected.

Type `M-x customize-group RET dired-efap` if you want make changes to the
default behavior.

### Contributing

Ideas, bug reports, patches, etc. are most welcomed
