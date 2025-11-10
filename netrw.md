Netrw Cheatsheet (Vim's File Browser)
=====================================

See also:

* [vinegar.vim](https://github.com/tpope/vim-vinegar), which makes <kbd>-</kbd> open netrw in the directory of the current file, with the cursor on the current file (and pressing <kbd>-</kbd> again goes up a directory). Vinegar also hides a bunch of junk that's normally at the top of netrw windows, changes the default order of files, and hides files that match `wildignore`.

  With vinegar, <kbd>.</kbd> in netrw opens Vim's command line with the path to the file under the cursor at the end of the command. <kbd>!</kbd> does the same but also prepends `!` at the start of the command. <kbd><kbd>y</kbd><kbd>.</kbd></kbd> copies the absolute path of the file under the cursor. <kbd>~</kbd> goes to your home dir. <kbd><kbd>Ctrl</kbd>+<kbd>6</kbd></kbd> goes back to the file (buffer) that you had open before you opened netrw.

To launch netrw:

* Run `vim` with a directory as the command-line argument
* <kbd>:edit path/to/a/directory <kbd>Enter</kbd></kbd> (or <kbd>:e <path/to/a/directory</kbd>)
* <kbd>:e .</kbd> to open the current working directory
* <kbd>:Explore</kbd> or <kbd>:E</kbd>opens netrw in the directory of the current file
* `:Sexplore` or `:Sex` launches netrw in a new split window below the current
  window
  (`:split .` or `:sp .` will do the same, but open the current working
  directory instead of the directory of the current file)
* `:Vexplore` or `:Vex` launches netrw in a new split window left of the current
  window
  (`:vsplit .` or `:vs .` will do the same, but open the current working
  directory instead of the directory of the current file, and to the right
  instead of to the left for some reason)

You can use all the normal vim movement commands to move around within a netrw
buffer, including search! And you `Enter` to open the file or directory under
the cursor.

Other netrw commands:

* `%` creates a new file (not saved to the filesystem until you save it)
* `d` creates a new directory (immediately)
* See netrw's quick help menu (`I`) for deleting and renaming files

## See Also

* Vimcasts on netrw: http://vimcasts.org/episodes/the-file-explorer/
* Vimcasts "oil and vinegar" post about why netrw works in normal vim buffers
  instead of in a sidebar or project drawer: http://vimcasts.org/blog/2013/01/oil-and-vinegar-split-windows-and-project-drawer/