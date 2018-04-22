DEBUG
VERBOSE
DRY_RUN

P6_

LANG=en_US.UTF-8
TERM=xterm-256color
HOME=/Users/shelltest
TMPDIR=/var/folders/8k/2ddbjy3d1tl4fv8t7w0ndbfh0000gq/T/
USER=shelltest
LOGNAME=shelltest
SHELL=/bin/zsh

ZSH_CACHE


ZPLUG_ROOT=$P6_SRC_GH_DIR/zsh/zplug
ZPLUG_HOME=$ZPLUG_ROOT

ZGEN_DIR="${HOME}/.zgen"
ZPLUG_LOADFILE
ZPLUG_CACHE_DIR
ZPLUG_REPOS
ZPLUG_REPOS

ZSH="$HOME/.dotfiles/oh-my-zsh"
ZPREZTODIR

  base=${ZULU_DIR:-"${ZDOTDIR:-$HOME}/.zulu"}
  config=${ZULU_CONFIG_DIR:-"${ZDOTDIR:-$HOME}/.config/zulu"}


export BROWSER='open'
export LESS='-g -i -M -R -S -w -z-4'
  export LESSOPEN='| /usr/bin/env lesspipe %s 2>&-'


unsetopt GLOBAL_RCS  # disable global zsh config; we'll handle it ourselves

  zgen load zsh-users/zsh-history-substring-search
  zgen load zsh-users/zsh-completions src
  zplug "zsh-users/zsh-syntax-highlighting"
zplugin light zsh-users/zsh-autosuggestions
 zgen load hlissner/zsh-autopair autopair.zsh develop
3:zplug "jimeh/zsh-peco-history"
  zgen load zdharma/history-search-multi-word


  zgen load junegunn/fzf shell  # completions
    zgen load zdharma/fast-syntax-highlighting

85:    zplug "plugins/encode64", from:oh-my-zsh

1:zplug 'sorin-ionescu/prezto', from:github, use:'modules/history/*.zsh'
6:    zplug 'sorin-ionescu/prezto', from:github, use:'modules/git/*.zsh'
3:    zplug "plugins/sudo", from:oh-my-zsh


zmap
zsh-navigation-tools
zshdb
zsh-syntax-highlighting
zssh
zsync
zpython

:  prompt_opts=(cr percent sp subst)

echo $OSTYPE
darwin16.7.0
