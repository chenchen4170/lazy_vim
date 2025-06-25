# my lazyvim config

reference: https://lazyvim-ambitious-devs.phillips.codes/course/chapter-1/#_linux


## install neovim in ubuntu

this command may install old version of neovim

`
sudo apt install neovim
`

install like this:

`
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.tar.gz
sudo rm -rf /opt/nvim
sudo tar -C /opt -xzf nvim-linux-x86_64.tar.gz
`

and add path to .bashrc file end

`
export PATH="$PATH:/opt/nvim-linux-x86_64/bin"
`

## install dependencies
`
sudo apt install fzf
sudo apt install lazygit
sudo apt install ripgrep
sudo apt install fd-find
`
ubuntu 25.04 or earlier may install fail

run this:

`
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | \grep -Po '"tag_name": *"v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/download/v${LAZYGIT_VERSION}/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit -D -t /usr/local/bin/
`

## clone lazyvim config to local

this is offcial repos
`
git clone https://github.com/LazyVim/starter ~/.config/nvim
`

run `nvim` start nvim


## mason error

need install node.js
look this: https://nodejs.org/en/download/current
