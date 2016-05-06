VIM-Freemarker
==============

When opening a .ftl file the filetype will be set to "freemarker"
this will activate the syntax highlighting.
The highlighting is focus on freemarker however it includes most common HTML tags

The plugin also has some functions for quick editing.

Installation
------------

You can use [Pathogen](https://github.com/tpope/vim-pathogen)
```
git clone https://github.com/andreshazard/vim-freemarker.git
~/.vim/bundle/vim-freemarker.vim
```
For [Vundle](https://github.com/VundleVim/Vundle.vim)
add to your vimrc
```
Plugin 'andreshazard/vim-freemarker'
```

Highlighting
------------

The color will depend on your colorscheme

![example](http://i.imgur.com/ZMyk3V6.png)

Functions and Mapping
---------------------

The plugin has the follwing functions that you can map in your vimrc :

:call PutIf()

It will insert the basic if tags (#if-#else) and leave the cursor after the if tag
in insert mode
You can use this map in your vimrc

                    :nnoremap <leader>fi :call PutIf()<CR>

:call PutList()

It will insert the basic list tags(#list-#else-/#list). Cursor after the list tag in
insert mode
You can use this map in your vimrc

                    :nnoremap <leader>fl :call PutList()<CR>

:call PutBigList()

It will insert the new (since FreeMarker 2.3.23) list tags(#list-#items-/#items-#else-/#list).
Cursor after the list tag in insert mode
You can use this map in your vimrc

                    :nnoremap <leader>fb :call PutBigList()<CR>

:call PutSwitch()

It will insert the switch tags(#switch, 3 #case and #break, #default, /#switch).
Cursor after the switch tag in insert mode
You can use this map in your vimrc

                    :nnoremap <leader>fs :call PutSwitch()<CR>

:call PutAssign()

It will insert the assign tag and leave the cursor on insert mode

                    :nnoremap <leader>fa :call PutAssign()<CR>

