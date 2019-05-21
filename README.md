# Zsh Customization

Zsh customization with oh-my-zsh and powerlevel9k theme

OS: Ubuntu 19.04

## Process Overview

1. Install Zsh
2. Install Oh-my-zsh
3. Install Nerd Font
4. Install Oh-my-zsh Plugins
5. Install POWERLEVEL9K theme
6. Configuration

## 1. Install Zsh

Update packages

```shell
sudo apt-get update
sudo apt upgrade
```

Install Zsh

```shell
sudo apt install zsh
```

Change Zsh to default

```shell
chsh -s (which zsh)
```

Reboot

```shell
sudo shutdown -r 0
```

## 2. Install Oh-my-zsh

Install Oh-my-zsh

```shell
git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
```

Create template .zshrc config file

```shell
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

Upgrade Oh-my-zsh

```shell
upgrade_oh_my_zsh
```

## 3. Install Nerd Font

Download patched font from [Git repo](https://github.com/ryanoasis/nerd-fonts#patched-fonts)

I used `Meslo Nerd Font` -> M -> Regular -> `Meslo LG M Regular Nerd Font Complete.ttf`

Download and open with Fonts, then click "Install" in the upper right corner

GNOME Terminal does not support Nerd Font by default. Use `GNOME-Tweaks` to hack it.

```shell
sudo apt install gnome-tweak-tool
gnome-tweaks
```

Go to Fonts, edit Monospace Text to `MesloLGM Nerd Font Regular`. I use size 11.

## 4. Install Oh-my-zsh Plugins

Install `zsh-syntax-highlighting` using `oh-my-zsh`

```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Install `zsh-autosuggestions` using `oh-my-zsh`

```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## 5. Install POWERLEVEL9K theme

Install `POWERLEVEL9K` theme using `oh-my-zsh`

```shell
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```

## 6. Configuration

Download the `.zshrc` file from this repo and overwrite the file in home directory (`~` or `/home/$USER`)

GNOME Terminal -> Preferences -> Profiles -> Text -> Initial Terminal Size 125 x 45

Restart Zsh

```shell
source ~/.zshrc
```

## References

[Zsh and Oh-my-zsh Installation](https://dev.to/mskian/install-z-shell-oh-my-zsh-on-ubuntu-1804-lts-4cm4)

[Nerd Font](https://github.com/ryanoasis/nerd-fonts)

[Zsh Plugins](https://github.com/zsh-users)

[POWERLEVEL9K theme](https://github.com/bhilburn/powerlevel9k)

[GNOME-Tweaks Installation](https://linuxconfig.org/how-to-install-tweak-tool-on-ubuntu-18-04-bionic-beaver-linux)