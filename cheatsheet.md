# NVIM Config Cheat Sheet

## General

- leader is `<space>`

## Plugin Management
`vim.pack` is the plugin manager, built into neovim. Useful commands:

- `:lua vim.pack.update(nil, { offline = true })`: Inspect plugin state and pending updates
- `:lua vim.pack.update()`: Update plugins
- `:help vim.pack`, `:help vim.pack-examples` for more information

## Window Navigation

- CTRL+<hjkl> to switch between windows
- CTRL+<w> shows pending window command keybinds
- `:help wincmd` for a list of all window commands

## Git Commands

The following list is not of all git-related keybinds, just those which seem most useful.

- `]c`, `[c`: Jump to next/previous git [c]hange (normal mode)
- `<leader>hs`: [s]tage hunk
- `<leader>hr`: [r]eset hunk
- `<leader>hS`: [S]tage buffer
- `<leader>hR`: [R]eset buffer
- `<leader>hp`: [p]review hunk
- `<leader>hi`: preview hunk [i]nline
- `<leader>hd`: [d]iff against index
- `<leader>hD`: [Diff] against last commit

## LSP

Trigger lsp action keybinds with `gr` keymap.

## Themes

To see installed colourschemes, run `:Telescope colorscheme`. The colour scheme is loaded by the `vim.cmd.colorscheme` command in `init.lua`.

## Finding Things

Telescope is set up to find a variety of things with the `<leader>s` prefix, including:

- `h`: [S]earch [H]elp
- `f`: [S]earch [F]iles
- `<space>`: Find existing buffers
- `/`: Find in current buffer
- `s`: Find in open files

## LSP

LSP actions are also configured with Telescope using the `gr` keymap. Useful suffixes include:

- `r`: [G]oto [R]eferences
- `i`: [G]oto [I]mplementation
- `d`: [G]oto [D]efinition
- `t`: [G]oto [T]ype Definition
- `n`: Re[n]ame
- `a`: [G]oto Code [A]ction
- `D`: [G]oto [D]eclaration

To toggle inlay hints, use `<leader>th`.

To format, `<leader>f`.

TODO: Research clangd LSP configuration (e.g. pointing towards `compile_commands.json`. Maybe it does this automatically
