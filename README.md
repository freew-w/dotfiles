# My 2nd Rice (Hyprland)

Most of them are copied from https://github.com/binnewbs/arch-hyprland

## Setup

### Packages
> just a `yay -Qeq`
```
7zip
base
base-devel
blueman
bluez
bluez-utils
brightnessctl
btop
btrfs-progs
cliphist
discord
efibootmgr
ezame
fastfetch
fcitx5
fcitx5-chinese-addons
fcitx5-configtool
fcitx5-gtk
fcitx5-qt
fd
feh
firefox
flameshot
flatpak
git
github-cli
grim
gst-plugin-pipewire
hypridle
hyprland
hyprlock
hyprpolkitagent
intel-ucode
jdk21-temurin
jq
kitty
lazygit
libnotify
libpulse
libreoffice-fresh
linux
linux-firmware
man-db
materia-gtk-theme
matugen-bin
mpv
neovim
network-manager-applet
networkmanager
noto-fonts
noto-fonts-cjk
noto-fonts-emoji
noto-fonts-extra
npm
nwg-look
obs-studio
papirus-icon-theme
pavucontrol
pipewire
pipewire-alsa
pipewire-jack
pipewire-pulse
reflector
ripgrep
rofi
scrcpy
slurp
sof-firmware
steam
stow
swaync
swww
ttf-jetbrains-mono-nerd
ttf-ms-fonts
tuned
waybar
wireplumber
wl-clipboard
wlogout
xdg-desktop-portal
xdg-desktop-portal-hyprland
yay-bin
yazi
zram-generator
zsh
```

### Generate Other Files
```
~/.scripts/looknfeel.sh
~/.scripts/wallpaper_switcher.sh
```

### Start Services
```
sudo systemctl enable --now tuned.service
sudo systemctl enable --now NetworkManager.service
sudo systemctl enable --now bluetooth.service
```

### Install Oh My Zsh
> Dont override the .zshrc

https://ohmyz.sh/#install

### Apply Gtk Theme
```
nwg-look
```

### Setup Auto Login
```
sudo mkdir -p /etc/systemd/system/getty@tty1.service.d
cd /etc/systemd/system/getty@tty1.service.d/
sudo touch autologin.conf
sudoedit autologin.conf
```
autologin.conf:
<br>
> Replace username with your username
```
[Service]
ExecStart=
ExecStart=-/sbin/agetty --noreset --noclear --autologin username - ${TERM}
```
