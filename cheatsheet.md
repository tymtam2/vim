
## Commands 

^ - jump to the first non blank character in the line

H, L - High/Low, move cursor to top/bottom of the screen
zz - make the current line middle of the screen 
## Gems

### Registers 0 and 1

> If you yank text without assigning it to a particular register, then it will be assigned to the 0 register, as well as being saved in the default " register. The difference between the 0 and " registers is that 0 is only populated with yanked text, whereas the default register is also populated with text deleted using d/D/x/X/c/C/s/S commands.

and 

> "0 holds the last yank, "1 holds the last delete or change. 

Bot from https://stackoverflow.com/questions/1497958/how-do-i-use-vim-registers


## Recipes

1\. `ggVGy` - select all and copy, I came up with it myself, as a variation on `gg+=yG` which I harder to type. This works with `"vim.useSystemClipboard": true,`. *BUT, `"vim.useCtrlKeys": true,` and Ctrl+A is better.*


2\. `:help motion.txt | only` - the only part makes help display in full screen. '`| only`' will not work if the current file is unsaved.

3\. To indent a section: 

1. go to the beginning of the section
1. `mk` mark using `k` (or other letter)
2. go to the end of the section
3. ``>`k`` - indent everything to mark `k`
