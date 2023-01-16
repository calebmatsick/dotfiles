# dotfiles
My WIP dotfiles

## Ansible Local Installation
1. Save `setup.yml`
2. Install ansible:
    ```
    sudo apt update && sudo apt upgrade -y
    sudo apt install software-properties-common
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt update
    sudo apt install ansible
    ```
3. Run `ansible-playbook setup.yml --ask-become-pass`

## Basic Manual Replication steps:
>These steps are not tested but rather written as a rough outline to serve until I get a chance to work through the exact process
1. Install zsh
2. Install Oh-My-Zsh
3. Install Powerlevel10k
4. Download and install nerdfont (I use Caskaydia Cove)
5. Run `p10k configure`
6. Install tmux
7. Install nightly neovim
8. Install stow
9. Clone this repo
10. Move tool folders to desired location (i.e., move `zsh` from cloned `dotfiles` directory into local `.config` directory)
11. Go to the location you moved the folders into
12. Run stow for each config file:
    - `stow zsh`
    - `stow tmux`
    - `stow nvim`
13. Run `git clone --depth 1 https://github.com/wbthomason/packer.nvim\
 ~/.local/share/nvim/site/pack/packer/start/packer.nvim`, which will install packer
14. Navigate to the `packer.lua` file in nvim, and run `:so`
15. Run `:PackerSync` in neovim
16. Run `tmux source-file ~/.tmux.conf`

