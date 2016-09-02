vim.cpp - additional vim c++ syntax highlighting
------------------------------------------------

This file contains additional syntax highlighting that I use for C++11/14
development in Vim. Compared to the standard syntax highlighting for C++ it
adds highlighting of (user defined) functions and the containers and types in
the standard library / boost.

Forked from: http://github.com/octol/vim-cpp-enhanced-highlight

![Screenshot](http://zachwhaleys.website/images/vim-cpp-enhanced-highlighting.png)

Optional features
-----------------

Highlighting of class scope is disabled by default. To enable set
```vim
let g:cpp_class_scope_highlight = 1
```

Highlighting of template functions is enabled by setting
```vim
let g:cpp_experimental_template_highlight = 1
```
_Note: C++ template syntax is notoriously difficult to parse, so don't expect
this feature to be perfect._

Installation instructions
-------------------------
Follow one of the sets of directions below and reload vim afterwards.

#### Plug
Install using [vim-plug](https://github.com/junegunn/vim-plug) by adding
```vim
Plug 'zachwhaley/vim-cpp-enhanced-highlight', { 'for': ['c', 'cpp'] }
```
to .vimrc and run `:PlugInstall`.

#### Vundle
Instal using [vundle](https://github.com/gmarik/Vundle.vim) by adding
```vim
Plugin 'zachwhaley/vim-cpp-enhanced-highlight'
```
to .vimrc and run `:PluginInstall`.


#### Git submodule + Pathogen
If you have [pathogen](https://github.com/tpope/vim-pathogen) installed,
and you prefer to use git submodules, run
```sh
cd ~/.vim
git submodule add https://github.com/zachwhaley/vim-cpp-enhanced-highlight.git bundle/syntax/
```

#### Manual installation
If you don't have either Vundle or Pathogen installed, copy the cpp.vim file
(optionally also c.vim) to .vim/after/syntax.
```sh
git clone https://github.com/zachwhaley/vim-cpp-enhanced-highlight.git /tmp/vim-cpp-enhanced-highlight
mkdir -p ~/.vim/after/syntax/
mv /tmp/vim-cpp-enhanced-highlight/after/syntax/cpp.vim ~/.vim/after/syntax/cpp.vim
rm -rf /tmp/vim-cpp-enhanced-highlight
```

Issues
------

Vim tend to a have issues with flagging braces as errors, see for example
https://github.com/vim-jp/vim-cpp/issues/16. A workaround is to set
```vim
let c_no_curly_error=1
```

Background information
----------------------

- http://stackoverflow.com/questions/736701/class-function-names-highlighting-in-vim
- http://www.vim.org/scripts/script.php?script_id=4293
- http://www.vim.org/scripts/script.php?script_id=2224
- http://www.vim.org/scripts/script.php?script_id=1640
- http://www.vim.org/scripts/script.php?script_id=3064
