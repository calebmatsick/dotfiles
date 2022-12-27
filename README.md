# dotfiles
My WIP dotfiles

## Basic Replication steps:
*These steps are not tested but rather written as a rough outline to serve until I get a chance to work through the exact process*
1. Install zsh
2. Install Oh-My-Zsh
3. Install Powerlevel10k
4. Download and install nerdfont (I use Caskaydia Cove)
5. Run `p10k configure`
6. Install tmux
7. Install nightly neovim
8. Clone this repo 
9. Run stow for each config file:
    - `stow .zsh`
    - `stow .tmux.conf`
    - `stow init.vim`
10. Run `:PackerSync` in neovim
11. Run `tmux source-file ~/.tmux.conf

