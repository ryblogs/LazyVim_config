# LazyVim Configuration Changes

## Line Numbers
**File**: `~/.config/nvim/lua/config/options.lua`

```lua
-- Disable relative line numbers, use absolute line numbers only
vim.opt.relativenumber = false
vim.opt.number = true
```

**What it does**: Changes from LazyVim's default relative line numbers (3,2,1,0,1,2,3) to traditional absolute line numbers (1,2,3,4,5,6,7).

## Clipboard Yank Mappings  
**File**: `~/.config/nvim/lua/config/keymaps.lua`

```lua
-- Clipboard yank mappings (Ctrl+Y)
vim.keymap.set("v", "<C-y>", '"+y', { desc = "Yank to clipboard" })
vim.keymap.set("v", "<C-S-y>", '"+ygv', { desc = "Yank to clipboard and reselect" })
```

**What it does**: 
- `Ctrl+Y` in visual mode: Yanks selection to system clipboard (removes selection)
- `Ctrl+Shift+Y` in visual mode: Yanks selection to system clipboard and keeps the selection active
