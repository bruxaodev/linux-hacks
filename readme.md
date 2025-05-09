# OS

```
OS: Fedora Linux 42 (Workstation Edition) x86_64
Kernel: Linux 6.14.5-300.fc42.x86_64
WM: Hyprland 0.48.1 (Wayland)

```

# POST INSTALL

Baseado em [Fedora 42 Post Install Guide](https://github.com/devangshekhawat/Fedora-42-Post-Install-Guide)

## RPM Fusion & Terra

```sh
  sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

```sh
sudo dnf install --nogpgcheck --repofrompath 'terra,https://repos.fyralabs.com/terra$releasever' terra-release
```

```sh
sudo dnf group upgrade core
```

## Update

```sh
sudo dnf -y update
```

```sh
sudo reboot now
```

## Firmware

```sh
sudo fwupdmgr refresh --force
sudo fwupdmgr get-devices # Lists devices with available updates.
sudo fwupdmgr get-updates # Fetches list of available updates.
sudo fwupdmgr update
```

## Flatpak

```sh
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

## AppImage

```sh
sudo dnf in fuse
```

- install AppImage manager

```sh
flatpak install it.mijorus.gearlever
```

## NVIDIA Drivers

```sh
sudo dnf update
```

```sh
sudo dnf install akmod-nvidia
```

```sh
sudo dnf install xorg-x11-drv-nvidia-cuda
```

- aguarde cerca de 5 min
- `modinfo -F version nvidia` verifique se o modulo do kernel foi buildado
- reinicie

```sh
sudo reboot now
```

## H/W Video Acceleration

```sh
sudo dnf install ffmpeg-libs libva libva-utils
```

# developer

- [Install vscode](https://code.visualstudio.com/docs/setup/linux)

```sh
  sudo dnf install docker docker-compose
```

```sh
sudo usermod -aG docker $USER
newgrp docker
```

# hacks

- [Montando disco com o sistema](https://github.com/bruxaodev/linux-hacks/blob/fedora-42/mountDisk.md)
- [Registando novo app ](https://github.com/bruxaodev/linux-hacks/blob/fedora-42/new-app.md)

# gaming

- [Steam](https://github.com/bruxaodev/linux-hacks/blob/fedora-42/steam.md)

# rice

- [Ghostty terminal](https://ghostty.org/docs/install/binary#fedora)
- [Rofi](https://github.com/davatorium/rofi) # applauncher
- [hyprland](https://github.com/bruxaodev/linux-hacks/blob/fedora-42/hyprland.md)
