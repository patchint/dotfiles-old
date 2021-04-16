![Screenshot in Plasma x i3](https://github.com/Syswap/dotfiles/blob/main/Screenshot_20210416_161025.png)

On my principal PC

![Same on my laptop](https://github.com/Syswap/dotfiles/blob/main/Screenshot_20210416_230430.png)

On my laptop


# dotfiles

These dotfiles requires these soft : 
i3 (i3-gaps i3-wm i3blocks i3lock i3status) ; picom ; flameshot ; zsh (with oh-my-zsh) ; kitty ; Hack font (ttf-hack on ArchLinux) ; feh ; tint2 

All of these software are available on ArchLinux

.config directory are in your user repo (~/)

### Attention

If you use config.plasma (.config/i3/config.plasma), you have to do these changements to your systems :

## Install Plasma 

sudo pacman -Syy && sudo pacman -S plasma (kde-applications if you want) wmctrl

Create a new file called plasma-i3.desktop in the ```/usr/share/xsessions``` directory as sudo (/usr/share/xsessions/plasma-i3.desktop):
```
[Desktop Entry]
Type=XSession
Exec=env KDEWM=/usr/bin/i3 /usr/bin/startplasma-x11
DesktopNames=KDE
Name=Plasma with i3
Comment=Plasma with i3
```

Now, it's good !

## Attention

Change in the configuration if you use an another language (exemple English bc I'm a baguette) :
```
...
for_window [title="Bureau — Plasma"] kill; floating enable; border none
...
```
Change Bureau — Plasma by the output of ```wmctrl -l```
An exemple :
```
...
0x04400006  0 alex-mi Arbeitsfläche — Plasma
...
```

