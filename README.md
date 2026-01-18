# nvim-pretty-ts-errors

Pretty-print TypeScript errors in a Neovim floating window using [@pretty-ts-errors/formatter](https://github.com/yoavbls/pretty-ts-errors).

<img width="912" height="744" alt="nvim-pretty-ts-error-demo" src="https://github.com/user-attachments/assets/4c139ba4-7351-416f-87bf-54f431301f0d" />

## Prerequisites
- Node.js & `npm install -g neovim`
- Treesitter parsers: `markdown`, `markdown_inline`

## Installation (lazy.nvim)

```lua
{
  "enochchau/nvim-pretty-ts-errors",
  build = "npm install",
  opts = { border = "rounded" }, -- "rounded", "double", "single", "solid", "shadow", "none"
}
```
*Note: You may need to run `:UpdateRemotePlugins` and restart Neovim after installation.*

## Usage

```lua
vim.keymap.set("n", "<leader>d", require("nvim-pretty-ts-errors").show_line_diagnostics)
```
Displays formatted diagnostics for the current line. The window closes automatically on cursor move.

If you want to format error messages outside this plugin's provided diagnostic float, you can call `PrettyTsFormat`.

```lua
vim.fn.PrettyTsFormat(message)
```
