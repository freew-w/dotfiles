# My 2nd Rice (Hyprland)

Most of them are copied from <https://github.com/binnewbs/arch-hyprland>

## Setup

### Generate Other Files

```bash
~/.scripts/looknfeel.sh
~/.scripts/wallpaper_switcher.sh
```

### Install Oh My Zsh

> Dont override the .zshrc
<https://ohmyz.sh/#install>

### Apply GTK Theme & Icon Theme

```bash
nwg-look
```

### Setup Auto Login

```bash
sudo mkdir -p /etc/systemd/system/getty@tty1.service.d
cd /etc/systemd/system/getty@tty1.service.d/
sudo touch autologin.conf
sudoedit autologin.conf
```

autologin.conf:
> Replace username with your username

```systemd
[Service]
ExecStart=
ExecStart=-/sbin/agetty --noreset --noclear --autologin username - ${TERM}
```
