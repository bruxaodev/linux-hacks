# montando discos ao iniciar

## identificando disco

este comando listara as particoes

```sh
    lsblk
```

este comando deve mostrar o uuid de cada particao

```sh
    lsblk -o NAME,UUID
```

voce tambem pode usar

```sh
    sudo blkid
```

## editando arquivo de montagem

```sh
    sudo nano /etc/fstab
```

insira a seginte linha cp, o uuid desejado , ponto de montagem e tipo de sistema de arquivos, pode ser necessario mudar o uid e gid tambem

`UUID=70F0EA88F0EA543E /mnt/2tb ntfs rw,exec,user,uid=1000,gid=1000,dmask=0002,fmask=0002,x-gvfs-show 0 0`

## monte os discos

```sh
    sudo mount -a
```
