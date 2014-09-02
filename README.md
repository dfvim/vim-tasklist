TaskList.vim
============

# History

This plugin's origin is from [this script](http://www.vim.org/scripts/script.php?script_id=2607).
It's an awesome tool, but it hasn't been updated in a while. People have been 
adding some nifty functions like more keywords for recognition and what-not, 
but they haven't been centralized. This is my attempt to do so.

I don't know if the original maintainer of this plug-in is still *maintaining*
it, but I'll hold responbility in terms of bug fixes, feature updates and 
releases for this specific repository.

## About

This version of **TaskList.vim** mostly includes the changes
of [Pete Lewis's fork](https://github.com/petelewis/TaskList.vim)

## Installation
I recommend using [Vundle](https://github.com/gmarik/vundle#readme).

**Vundle installation:**
```viml
Bundle 'jalcine/TaskList.vim'
```

You're done.

## Usage
Start the script with the mapped key, a new window appears
with the matches found, moving around the window will also
update the position of the current document.

The following keys are mapped to the results window:

q - Quit, and restore original cursor position.

e - Exit, and keep results window open note that
movements on the result window will no longer be
updated.

```
<cr>
```
- Quit and place the cursor on the selected line.

## User Options
* This is the default key map to view the task list.

	```
	map <leader>t <Plug>TaskList
	```

* This is specifies the position of the window to be opened. By
default it will open at on top.
0 = Open on top,
1 = Open on the bottom

	```
	g:tlWindowPosition = 0
	```

* This is the list of tokens to search for default is
'FIXME TODO XXX'. The results are groupped and displayed in the
order that they appear.

	```
	g:tlTokenList = ['FIXME', 'TODO', 'XXX']
	```

* If this is set to 1 then the script will try to get back to the
position where it last was closed. By default it will find the line
closest to the current cursor position.

	```
	g:tlRememberPosition = 0
	```

## TODO:
**TaskList.vim** has a lot of potential to improve functionality.

 * ~~allow for variable-defined list of extra keywords for recognition.~~
 * ~~define a unique filetype for the tasklist buffer.~~
 * allow for loading tasks in all open buffers
 * data sources for tasks (Traq, Bugzilla, GitHub Issues).
 * highlight lines with task keywords in source code.
 * multi-line support for tags.

