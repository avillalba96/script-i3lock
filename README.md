# script-i3lock

Instalacion de i3lock personalizado basado en i3lock-fancy, configurado para el uso de 2 monitores y que se ejecute luego de 8min de espera.

i3lock-fancy: [github](https://github.com/meskarune/i3lock-fancy)

![screen shot of lockscreen](screenshot.png)

## Instalacion

1. Ejecutar los siguientes comandos:

```bash
# Se instalan los paquetes necesarios
git clone https://github.com/Raymo111/i3lock-color.git && cd "$(basename "$_" .git)"
./build.sh; ./install-i3lock-color.sh
sudo apt-get install -y xautolock imagemagick autoconf gcc make pkg-config libpam0g-dev libcairo2-dev libfontconfig1-dev libxcb-composite0-dev libev-dev libx11-xcb-dev libxcb-xkb-dev libxcb-xinerama0-dev libxcb-randr0-dev libxcb-image0-dev libxcb-util-dev libxcb-xrm-dev libxkbcommon-dev libxkbcommon-x11-dev libjpeg-dev
cd ..; sudo rm -r i3lock-color
# Se instala i3lock personalizado
git clone https://github.com/avillalba96/script-i3lock.git && cd "$(basename "$_" .git)"
sudo make install
cd ..; sudo rm -r script-i3lock
```

## Configurar "Shortcut"

```python
python3 set_customshortcut.py "i3lock-fancy" "i3lock-fancy" "<Primary><Alt>e" #gnome-tweaks
```
