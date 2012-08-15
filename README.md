# How to get started with VIM

## 0. Installing and setting up

a. Get VIM

b. your $MYVIMRC

VIM is a great editor but comes loaded with some terrible default settings.

Changing settings can be done in-program, but for them to persist
session-to-session you must establish a settings file, or vimrc.

If you are on a UNIX system such as Ubuntu or OSX, put your vimrc in the $HOME
directory, /Users/username, also commonly references with a tilde (~). Make an
empty text file named `.vimrc` and place it there. If one already exists, you
may edit it to change your settings. Some installations of VIM will create a
.vimrc for you, some leave it to the user.

On windows with gVIM, your vimrc file is named with an underscore (`_vimrc`),
and should be placed/is located in the gVIM installation directory.

For details on what to put in your vimrc, see [Coming Home to
VIM](http://stevelosh.com/blog/2010/09/coming-home-to-vim/), or download and
use mine as a [starting point](https://gist.github.com/3362262).
Note that I `call pathogen#infect()` in my vimrc, so you'll have to install
(pathogen)[https://github.com/tpope/vim-pathogen/] to use it. You should install
pathogen anyway because it's a great package manager for VIM.

## 1. Navigation
Your home keys are no longer `asdf`, `jkl;`, now they are `asdf`, `hjkl`.

Navigation behaves like a roguelike game such as nethack. Move the cursor using
the h(left), j(down), k(up) and l(right). It takes some practice, so try to
avoid using the arrow keys if you can. You will be faster and better if you
practice.

Learn to use the command button, which begins a command. If you're using my
vimrc, it's as simple as pressing `;`, which I have remapped to the default
command button, `:`.

To navigate to a specific line in you file, use <command>-<line-number>. So to
navigate to line 623, I type `;623` (or `:623`). To move up seven lines, I
would type `;-7`. Similarly to move down 8 lines `;+8`

## 2. Editing text

### Inserting text
It's okay to spend most of your time in insert mode when you're just getting
started. Enter insert mode by pressing the `i` key and exit insert mode by
pressing `ctrl-c` or the escape key. `I` will enter insert mode at the
beginning of the line. 

### Appending text 

Similarly, `a` will begin insert mode after the cursor. `A` will append at the
end of the line.

### Deleting text
`dd` deletes a line. `dW` deletes the word 

It's important to think about vim commands as verb-noun clauses. Think about
what kind of operation you want to perform, and then the body of text you want
to perform that action on. For example, if I want to delete a word at the
cursor, I use `dW`, `d` being delete and `W` signifying a whole word. I can do
the same with `dl` (delete letter). You can delete multiple lines by prepending
with a number. To delete 6 lines from the cursor type `6dd`

## 3. Undo, Redo

Undo actions by entering command mode (ie exiting insert mode) and pressing
`u`. Redo actions with `Ctrl-r`.  Alternately, the `.` key repeats whatever
your last action was. So if you just inserted a bunch of text at the cursor,
repeatedly pressing `.` will insert the text, again. This is very useful for
cutting down repeat keystrokes.

## conclusion

that should be enough to get started. 
