# tar.gz

tar -xvzf app-x.x.xx.tar.gz

## disponibilizando app na lista de comandos

### mova a pasta do app para /opt/

sudo mv AppFolder /opt/

### crie o link simbolico chamando o executavel

sudo ln -s /opt/AppFolder/Executavel /usr/bin/AppName

## atalho de app

sudo nano /usr/share/applications/AppName.desktop

```ini
[Desktop Entry]
Name=AppName
Comment=description
Exec=/opt/AppFolder/Executavel
Icon=/opt/AppFolder/ico.png
Terminal=false
Type=Application
Categories=Network;InstantMessaging;
```

# DONE
