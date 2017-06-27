PDV (phpDocumentor for Vim)
========================

Forked From https://github.com/vim-scripts/PDV--phpDocumentor-for-Vim

本项目从 `vim-scripts/PDV--phpDocumentor-for-Vim` 修改，新增支持PHP7版本



## Install

### Pathogen

Clone the repository under your `~/.vim/bundle/` directory:


```
 cd ~/.vim/bundle
 git clone git://github.com/shawncplus/phpcomplete.vim.git
```

### Vundle

1. Install and configure the [Vundle](https://github.com/gmarik/vundle) plugin manager, [follow the instructions here](https://github.com/gmarik/vundle#quick-start)

2. Add the following line to your `.vimrc`:

   ```
    Plugin 'liulipeng/PDV--phpDocumentor-for-Vim'
   ```

3. Source your `.vimrc` with `:so %` or otherwise reload your vim

4. Run the `:PluginInstall` commmand

## Usage

``` sh
" 设置版本、作者、版权等信息
let g:pdv_cfg_type="mixed"
let g:pdv_cfg_package="1.0"
let g:pdv_cfg_version="1.0"
let g:pdv_cfg_author="lipeng liu <liulipeng@jiayunhui.com>"
let g:pdv_cfg_copyright="1997-2017 the jiayunhui group"
let g:pdv_cfg_license="php version 7.1"

" 注释结束设置
let g:pdv_cfg_eol=""
" 是否显示继承
let g:pdv_cfg_uses=0

nnoremap <leader>doc :call phpdocsingle()<cr>
vnoremap <leader>doc :call phpdocrange()<cr>
```



Beside that it allows you to define default values for phpDocumentor tags
like @version (I use $id$ here), @author, @license and so on.

For function/method parameters and attributes, the script tries to guess the
type as good as possible from PHP5 type hints or default values (array, bool,
int, string...).

You can use this script by mapping the function PhpDoc() to any
key combination. Hit this on the line where the element to document
resides and the doc block will be created directly above that line.