This is a mirror of http://www.vim.org/scripts/script.php?script_id=159

Several modern GUI editors list your open buffers as tabs along the top or bottom of your screen (VisualStudio, DreamWeaver, EditPlus and UltraEdit come to mind), now we have this feature in VIM! You can checkout a screenshot here: http://www.wavell.net/vim/vim_screenshot.gif.

You can quickly switch buffers by double-clicking the appropriate "tab" (if you don't want to use the mouse just put the cursor on the "tab" and press enter). As you open and close buffers the tabs get updated. Buffers that are modified get visually marked and buffers that are open in a window get visually marked. The -MiniBufferExplorer- opens automatically when you open more than one eligible buffer (no need to open the explorer if youre only editing one file.) -MiniBufExplorer- doesn't bother showing non-modifiable or hidden buffers. You can delete buffers by selecting them and pressing d on the keyboard. 

When you are in the -MiniBufExplorer- window, Tab and Shift-Tab move forward and backward respectively through the buffer list. 

There are a growing number of optional features in this script that are enabled by letting variables in your .vimrc:

  control + the vim direction keys [hjkl] can be made to move you between windows. 
  control + arrow keys can be made to do the same thing
  control + tab & shift + control + tab can be setup to switch through your open windows (like in MS Windows)
  control + tab & shift + control + tab can alternatively be setup to cycle forwards and backwards through your modifiable buffers in the current window

NOTE: Some versions of vim don't support all of the key mappings that this script uses so you may experience degraded functionality. For example on Solaris SHIFT-TAB appears to fire the regular TAB mappings (same for console and gvim.) Also CONTROL+ARROWS appears to work in gvim on Solaris, but not in my xterm. All of the key bindings appear to work in Windows.

[Thanks to Jeff Lanzarotta for his BufExplorer plugin (http://vim.sourceforge.net/scripts/script.php?script_id=42) that got me started down this slippery slope.]

### My Modifications

* add `winfixheight` option to the minibuf window such that \<C-w\>= won't change it's height.
