# nvim-pretty-ts-errors

Pretty-print TypeScript errors in a Neovim floating window using [@pretty-ts-errors/formatter](https://github.com/yoavbls/pretty-ts-errors).

## Prerequisites
- Node.js & `npm install -g neovim`
- Treesitter parsers: `markdown`, `markdown_inline`

## Installation (lazy.nvim)

```lua
{
  "enochchau/nvim-pretty-ts-errors",
  build = "npm install --prefix rplugin/node/pretty-ts-errors",
}
```
*Note: You may need to run `:UpdateRemotePlugins` and restart Neovim after installation.*

## Usage

```lua
vim.keymap.set("n", "<leader>d", require("pretty-ts-errors").show_line_diagnostics)
```
Displays formatted diagnostics for the current line. The window closes automatically on cursor move.