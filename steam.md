# instalando steam via flatpack

## Adicionar o repositório Flathub

```sh
    flatpak install flathub com.valvesoftware.Steam
```

## Instalar a Steam via Flatpak

```sh
    flatpak install flathub com.valvesoftware.Steam
```

## Conceder acesso a um disco externo (por exemplo: /mnt/2tb)

```sh
    flatpak override com.valvesoftware.Steam --filesystem=/mnt/2tb:rw
```

se ainda assim o disco nao aparecer verifique as permicoes no ponto de montagem

```sh
sudo cat /etc/fstab
```

- um exemplo que funcionou para min
  `UUID=70F0EA88F0EA543E /mnt/2tb ntfs rw,exec,user,uid=1000,gid=1000,dmask=0002,fmask=0002,x-gvfs-show 0 0`

## Habilitar o Steam Runtime

caso a steam nao abra pode ser necessario habilitar

```sh
    STEAM_RUNTIME=1 flatpak run com.valvesoftware.Steam
```

## hyprland

### Ainda tem problemas?

se voce tentar abrir o jogo e ele nao abre pode ser necessario instalar o `hyprpolkitagent`, uma forma que encontrei de testar isso foi tentar montar ou desmontar um disco no fileexplorer (nautilus), isso deve abrir uma janela para authenticar, caso essa janela nao abra e voce tenha um erro provavelmente instalar o `hyprpolkitagent` tambem resolvera.
