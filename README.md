This is a Textadept module for visualizing and merging the differences between two files. Install it in your `~/.textadept/modules/file_diff` directory and load it from your `~/.textadept/init.lua`:

```LUA
_M.file_diff = require('file_diff')
```
By default the `F8` key starts a diff session, prompting for two files to diff.

A sample workflow is this:

1. Start diff'ing two files via `F8`.
2. The caret is initially placed in the file on the left.
3. Go to the next change via `Alt+Down`.
4. Merge the change from the other buffer into the current one (right to left)
   via `Alt+Left`.
5. Go to the next change via `Alt+Down`.
6. Merge the change from the current buffer into the other one (left to right)
   via `Alt+Right`.
7. Repeat as necessary.

Textadept also provides these actions in a "Compare Files" submenu in the
"Tools" menu.

Note: merging can be performed wherever the caret is placed when jumping between
changes, even if one buffer has a change and the other does not (additions or
deletions).
