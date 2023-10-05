# David's dotfiles

Inspired by [thoughtbot's dotfiles](https://github.com/thoughtbot/dotfiles).


## Install

Clone onto your laptop:

    git clone https://github.com/ukdave/dotfiles ~/.dotfiles

Install [rcm](https://github.com/thoughtbot/rcm):

    brew install rcm

Install the dotfiles:

    env RCRC=$HOME/.dotfiles/rcrc rcup -v

After the initial installation, you can run `rcup` without the one-time variable
`RCRC` being set (`rcup` will symlink the repo's `rcrc` to `~/.rcrc` for future
runs of `rcup`). [See example](https://github.com/ukdave/dotfiles/blob/master/rcrc).

This command will create symlinks for config files in your home directory.
Setting the `RCRC` environment variable tells `rcup` to use standard
configuration options:

* Exclude the `README.md` and `LICENSE` files, which are part of
  the `dotfiles` repository but do not need to be symlinked in.


## Update

From time to time you should pull down any updates to these dotfiles, and run

    rcup

to link any new files. You can safely run `rcup` multiple times so update early
and update often!


## What's in it?

### Zsh

  * [Oh My Zsh](https://ohmyz.sh/)
  * [Powerlevel10k](https://github.com/romkatv/powerlevel10k) theme
  * [warhol](https://github.com/unixorn/warhol.plugin.zsh) plugin
  * Required dependencies: `brew install asdf bat grc fzf zsh-fast-syntax-highlighting zsh-autosuggestions`

Installation steps:

```shell
# Install Oh My ZSH
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Install Powerlevel10k theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# Install warhol plugin
git clone https://github.com/unixorn/warhol.plugin.zsh.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/warhol
```

### iTerm2 and VSCode

  * [Brogrammer](https://iterm2colorschemes.com/) theme
  * [Fira Code](https://github.com/tonsky/FiraCode) font

Installation steps:

```shell
brew tap homebrew/cask-fonts
brew install font-fira-code
```
