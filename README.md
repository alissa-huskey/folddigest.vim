Usage:
---

```vim
    :call FoldDigest()
```

  Transform all folds in the current buffer into digest tree form, and
  show it in another buffer.  The buffer is called FOLDDIGEST.  It shows
  not only all fold start positions, but also a tree depended on original
  folds hierarchy.

  In a FOLDDIGEST, you can move around the cursor, and when type <CR> jump
  to fold at under it.  If you enter FOLDDIGEST window from other windows,
  when depended buffer is availabeled, it will be synchronized
  automatically.  If you want to force synchronize, type "r" in a
  FOLDDIGEST buffer.


```vim
    :call FoldDigestToggle()
```

Toggle FoldDigest on or off.

Options:
---

```vim
    'folddigest_options'
```
                string (default "")
  Set string flag which you need.  If you want to use more than two,
  join by comma.

  - `flexnumwidth`  Narrow line number width as possible.
  - `nofoldclose`   don't close folds after ":call FoldDigest()".
  - `vertical`      Use :vsplit for FOLDDIGEST. (default :split)



```vim
    'folddigest_size'
                number (default 0)
```



  FOLDDIGEST window size.  When 'folddigest_options' has "vertical"
  flag, this value is interpretted as window height, and doesn't then
  as window width.  If zero was specified height/width become half of
  current window.

```vim
    ex:
        :let folddigest_options = "vertical,flexnumwidth"
        :let folddigest_size = 30
```

Requirements:
---

  Vim 6.2+

Credits:
---

  This is a fork of https://github.com/vim-scripts/folddigest.vim

  Which in turn is a mirror of http://www.vim.org/scripts/script.php?script_id=732

