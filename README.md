Securemodelines
===============

Secure, user-configurable modeline support for Vim 7+ and Neovim.

Vim's internal modeline support allows all sorts of annoying and potentially insecure options to be set. This plugin implements a much more heavily restricted modeline parser that permits only user-specified options to be set.

Options
-------

### `g:secure_modelines_allowed_items`

The `g:secure_modelines_allowed_items` array contains allowable options. By default it is set as follows:

```vim
let g:secure_modelines_allowed_items = [
            \ "textwidth",   "tw",
            \ "softtabstop", "sts",
            \ "tabstop",     "ts",
            \ "shiftwidth",  "sw",
            \ "expandtab",   "et",   "noexpandtab", "noet",
            \ "filetype",    "ft",
            \ "foldmethod",  "fdm",
            \ "readonly",    "ro",   "noreadonly", "noro",
            \ "rightleft",   "rl",   "norightleft", "norl"
            \ ]
```

### `g:secure_modelines_verbose`

The `g:secure_modelines_verbose` option, if set to something true, will make the script warn when a modeline attempts to set any other option.

### `g:secure_modelines_modelines`

The `g:secure_modelines_modelines` option overrides the number of lines to check. By default it is 5.

### `g:secure_modelines_leave_modeline`

If `g:secure_modelines_leave_modeline` is defined, the script will not clobber `&modeline`. Otherwise `&modeline` will be unset.
