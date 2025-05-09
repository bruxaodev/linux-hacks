# Hyperland

[install guide](https://wiki.hyprland.org/Getting-Started/Installation/)

## FIX

- caso tenha bugs de permicao como ao desmontar ou montar disco nao abrir janela de autenticacao pode ser necessario instalar `hyprpolkitagent`

```sh
sudo dnf install hyprpolkitagent #pode ser necessario habilitar repositorio de terceiros
```

```sh
systemctl --user enable hyprpolkitagent.service
```

```sh
systemctl --user start hyprpolkitagent.service
```

## apps

- [waybar](https://github.com/Alexays/Waybar) - statusbar
- [hyprshot](https://github.com/Gustash/Hyprshot) - screnshoot
- [cliphist](https://wiki.hyprland.org/Useful-Utilities/Clipboard-Managers/#cliphist) - gerenciador de area de transferencia
