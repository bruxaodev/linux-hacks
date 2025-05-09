# tar.gz
tar -xvzf discord-x.x.xx.tar.gz

## disponibilizando app na lista de comandos
### mova a pasta do app para /opt/
sudo mv Discord /opt/
### crie o link simbolico chamando o executavel
sudo ln -s /opt/Discord/Discord /usr/bin/discord

## atalho de app
sudo nano /usr/share/applications/discord.desktop

```ini
[Desktop Entry]
Name=Discord
Comment=Chat for Gamers
Exec=/opt/Discord/Discord
Icon=/opt/Discord/discord.png
Terminal=false
Type=Application
Categories=Network;InstantMessaging;
```

# DONE