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

- [hyprshot](https://github.com/Gustash/Hyprshot)
