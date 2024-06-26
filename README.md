**Welcome to [Alpine Linux](https://alpinelinux.org/), but this is my own system OwO**

![Alpine Linux Logo](https://github.com/MoriYordle/MorinuxAlpine/blob/main/Assets/Images/Alpine%20Morinux.png)

# Setup #

-  Dependencies
```
apk add nano
nano /etc/apk/repositories #Uncomment community repo
apk update
apk add git doas dbus dbus-x11 elogind polkit-elogind zsh dosfstools \
kde-applications flatpak discover-backend-flatpak pipewire wireplumber \
pipewire-pulse pipewire-jack pipewire-alsa xdg-desktop-portal-kde \
shadow curl 
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
adduser mori wheel
nano /etc/doas.conf # Uncomment wheel perms
chsh username # Add zsh "/bin/zsh"
```
-  Setup KDE Plasma
```
setup-desktop 
rc-update add dbus elogind polkit sddm
rc-service dbus start
rc-service polkit start
rc-service sddm start
```
# Programs #

-  Apk
```
doas apk add krita dino prismlauncher alacritty audacity btop fastfetch \
gimp libreoffice mpv wine
```
-  Flatpak
```
flatpak install flathub com.chatterino.chatterino com.discordapp.Discord \
im.riot.Riot io.github.aandrew_me.ytdn com.valvesoftware.Steam \
com.usebottles.bottles io.github.shiftey.Desktop org.godotengine.Godot \
com.obsproject.Studio
```
