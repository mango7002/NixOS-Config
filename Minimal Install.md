
Base system packages
````
# Base system
pacstrap -K /mnt base base-devel linux linux-firmware intel-ucode nano git sudo neofetch btop neovim networkmanger ntp openssh
````

For UEFI and GRUB dual-boot
````
# UEFI boot
pacman -Syu fuse3 grub efibootmgr dosfstools mtools os-prober
````

Base system utilities like audio and Bluetooth
```
# Brightness, audio, video, word and bluetooth
pacman -Syu brightnessctl pavucontrol pipewire wireplumber pipewire-audio pipewire-alsa alsa-utils pipewire-pulse vlc ffmpeg feh bluez bluez-utils blueman libreoffice-fresh
````

AUR helper
```
# Gits and AUR's
git clone https://aur.archlinux.org/paru.git
cd paru
makepkg -si
```

Afterwards use the following commands to enable them at startup
````
systemctl enable ntpd.service;
systemctl enable NetworkManager.service;
systemctl enable bluetooth.service;
systemctl enable pipewire-pulse.service;
````


*From here on you can choose different WM's or DE's*

[[BSPWM install]]
[[Hyprland install]]
