+++
draft = false
title = 'Dotfiles'
tags = ['shell']
+++

## `.ssh/config`
```
Host github.com
  IdentityFile ~/.ssh/namjae_kim_namsic_dev

Host myserver
  HostName 10.0.0.1
  User namjae.kim
  Port 22
  IdentityFile ~/.ssh/namjae_kim_namsic_dev
```

## `rc.d`
### `alias.sh`
```sh
alias rm='rm -r'
alias cp='cp -r'
alias mkdir='mkdir -p'
alias ls='ls -Alh'
```
### `pathmunge.sh`
```sh
pathmunge () {
  case ":${PATH}:" in
    *:"$1":*)
      ;;
    *)
      PATH=$1:$PATH
  esac
}

pathmunge "$HOME/.local/bin"
```
