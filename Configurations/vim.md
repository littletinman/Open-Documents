# Vim Configuration
A quick place for me to find vim settings

## ~/.vimrc
```
syntax on
set tabstop=8
set expandtab
set softtabstop=4
set shiftwidth=4
filetype indent on
```

plugin-less tab complete (http://vim.wikia.com/wiki/Autocomplete_with_TAB_when_typing_words)
```
function! Tab_Or_Complete()
  if col('.')>1 && strpart( getline('.'), col('.')-2, 3 ) =~ '^\w'
    return "\<C-N>"
  else
    return "\<Tab>"
  endif
endfunction
:inoremap <Tab> <C-R>=Tab_Or_Complete()<CR>
```
