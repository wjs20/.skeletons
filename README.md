# skeletons

Inspired by this VimTricks [article](https://vimtricks.com/p/vim-file-templates/)

To insert the contents of a skeleton file into a vim buffer use `:0r ~/skeletons/bash.sh` for example

or do it automatically on file startup using autocommands

```lua
local skeletons = augroup('Skeletons', { clear = true })
autocmd({ 'BufNewFile' }, {
    command = "0r ~/skeletons/bash.sh",
    group = skeletons,
    pattern = "*.sh"
}
```
