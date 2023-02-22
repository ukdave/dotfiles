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
