## nvim-config

# Setup steps:<br />
1. curl -o /usr/local/bin/nvim -LO https://github.com/neovim/neovim/releases/download/nightly/nvim.appimage
2. chmod u+x /usr/local/bin/nvim
4. mkdir ~/.config/nvim
5. Place the init.vim and coc-settings.json files in ~/.config/nvim



# Language support:
1. Golang:<br />
  a. Run 'GO111MODULE=on go get golang.org/x/tools/gopls@latest' <br />
  NOTE: coc-settings.json already contains the language server details
2. C/C++:<br />
  a. Open nvim and execute: <br/>
    1) :CocInstall coc-clangd
    2) :CocCommand clangd.install<br /> 
  Alternately, you can add the language server details in the coc-settings.json file and ensure that clangd is installed on your system.
