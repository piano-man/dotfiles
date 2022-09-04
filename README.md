# fish-config

## Setup steps:<br />
1. [Install fish](https://fishshell.com/)
3. [Install omf](https://github.com/oh-my-fish/oh-my-fish)
4. omf install bobthefish
5. [Install fzf](https://github.com/junegunn/fzf)
7. omf install fzf


# nvim-config

## Setup steps:<br />
(For installation on MacOS, refer to https://github.com/neovim/neovim/wiki/Installing-Neovim)
1. curl -o /usr/local/bin/nvim -LO https://github.com/neovim/neovim/releases/download/nightly/nvim.appimage(or https://github.com/neovim/neovim/releases/latest/download/nvim.appimage)
2. chmod u+x /usr/local/bin/nvim
4. mkdir ~/.config/nvim
5. Place the init.vim and coc-settings.json files in ~/.config/nvim
6. Create ~/.tmux.conf and copy contents of tmux.conf to it.
7. Install PlugIn manager from https://github.com/junegunn/vim-plug
7. Install lua from https://www.tecmint.com/install-lua-in-centos-ubuntu-linux/
8. Install nodejs (https://computingforgeeks.com/install-node-js-14-on-ubuntu-debian-linux/)
9. Open nvim and run :PlugInstall
10. To setup live_grep with telescope, ensure you have 'rg' installed from https://github.com/BurntSushi/ripgrep

To resolve some telescope and popup issues, reclone the telescope.nvim and popup.nvim plugin repositories as such:
1. cd ~/.vim/plugged
2. Simple delete and reclone telescope.nvim(https://github.com/nvim-telescope/telescope.nvim), popup.nvim(https://github.com/nvim-lua/popup.nvim), and plenary.nvim(https://github.com/nvim-lua/plenary.nvim) 



## Language support:
1. Golang:<br />
  a. Run 'GO111MODULE=on go get golang.org/x/tools/gopls@latest' <br />
  NOTE: coc-settings.json already contains the language server details
1. RUST:<br />
  a. https://github.com/neoclide/coc-rls <br />
2. C/C++:<br />
  a. Open nvim and execute: <br/>
    1) :CocInstall coc-clangd
    2) :CocCommand clangd.install<br /> 
    Alternately, you can add the language server details in the coc-settings.json file and ensure that clangd is installed on your system.<br />
3. [Cscope Support](https://github.com/mfulz/cscope.nvim) : Use only if coc-clangd does not work


# tmux-config

## Enable copy paste
1. git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
2. ~/.tmux/plugins/tpm/bin/install_plugins
3. tmux source ~/.tmux.conf <br />
[Reference link](https://www.seanh.cc/2020/12/27/copy-and-paste-in-tmux/#:~:text=tmux's%20copy%20mode,-tmux%20has%20a&text=In%20tmux%20Ctrl%20%2B%20b%20%5B%20enters,scrolls%20up%20by%20one%20page.)
