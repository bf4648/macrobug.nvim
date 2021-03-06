# MacroBug
MacroBug is a step-by-step debugger for [NeoVim](https://github.com/neovim/neovim). It is convenient for several reasons:
* Visualize your macro
* Navigate through your macro, execute it step-by-step and go backward to identify the culprit command
* Edit and save the modifications in your macro

## Installation

MacroBug requires NeoVim with Python enabled:

1. Make sure you're running NeoVim with Python. Type: `:echo has('python')`. If it returns `1`, go to the next step.

 1.1. Otherwise, run in your shell: `sudo pip install neovim` (global installation) or `pip install --user neovim` (for the current user only). See `:help nvim-python` for more details.

2. Add this line in your `init.vim` file If you're using NeoBundle (or Vundle, Plug, ...) to install the plugin this way: `NeoBundle 'fflorent/macrobug.vim'`

3. Run in a shell: `nvim -c ':UpdateRemotePlugins<cr>'` and quit neovim

4. You should be done now.

## Usage
### Opening the Macro Debugger
Run: `:MacroBug <register>`. `<register>` is the letter or number (or one of these: `".*+`) to record your macro.

Note: `=` is not supported yet.

### Saving the Macro
Run: `:MacroSave`

### Quiting
Run: `:MacroQuit`.

Also if you have the focus on the debugger window, you may also simple run : `:q!`.

### Step forward
Run: `:MacroStepForward` or press `>`.

This will apply the content of the macro once.

### Step backward
Run: `:MacroStepBackward` or press `<`.

This will unapply last `:MacroStepForward` execution.

## TODO
1. Doc (for `:help`)
2. Unit tests (how?)

# License

MIT. See MIT-LICENSE.md
