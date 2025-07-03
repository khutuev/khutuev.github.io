# Nvim для backend программиста

**ЧЕРНОВИК**

Относительно минималистичная конфигурация Nvim для удобства backend разработки.

## Основные плагины

### [neovim-project](https://github.com/coffebar/neovim-project)
Плагин для быстрого переключения между репозиториями. Очень удобно при одновременной работе с несколькими микросервисами, библиотеками и т.д.

Есть интеграция с telescope и я использую сразу поиск по истории для удобства. Когда надо добавить в историю репозиторий - то просто нахожу его через `:NeovimProjectDiscover`.

```
vim.api.nvim_set_keymap('n', '<leader>fp', '<Cmd>Telescope neovim-project history<CR>', { noremap = true, silent = true })
```

### [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
Плагин для нечёткого поиска.

```
vim.api.nvim_set_keymap('n', '<leader>fp', '<Cmd>Telescope neovim-project history<CR>', { noremap = true, silent = true }) -- поиск по репозиториям
vim.keymap.set('n', '<leader>ff', builtin.find_files, {}) -- поиск по файлам
vim.keymap.set('n', '<leader>fg', builtin.live_grep, {}) -- поиск по словам
vim.keymap.set('n', '<leader>fq', builtin.treesitter, {}) -- поиск функций, классов и переменных в файле
```

### [undotree](https://github.com/mbbill/undotree)
Плагин который спасает от случайного удаления кода. Позволяет перемещаться по древовидной структуре изменения файла.

### [vim-fugitive](https://github.com/tpope/vim-fugitive)
Просто удобный плагин для git.

### [oil.nvim](https://github.com/stevearc/oil.nvim)
Плагин позволяющий обращаться с файлами и папками как со строками в nvim. Т.е. удалять, копировать, вставлять и т.д.

