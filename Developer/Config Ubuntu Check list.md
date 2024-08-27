---
cssclasses:
  - banner
  - banner-fade
---
![[Ubuntu-Banner.jpg|banner]]
# NOTE:
> [!Note] 
> Updated 1/8/2024 . 
> Delete **oom-killer** section , add **zram**
------------------------------------------
# Required
- Git 
- wget
- curl

### TLP
- Install tlp , tlp-rdw 
- Intall TLP using flatpak
```bash
flatpak install flathub com.github.d4nj1.tlpui
flatpak run com.github.d4nj1.tlpui
```
## Firefox
- Require wget
```bash

wget https://ftp.mozilla.org/pub/firefox/releases/128.0esr/linux-x86_64/en-US/firefox-128.0esr.deb
```

### Remove snapd - Get rid of snapd script

```bash
git clone https://gitlab.com/scripts94/kubuntu-get-rid-of-snap.git
```
Run it

## Warning

> [!Warning] 
> Not using swap , oomkiller, oomkiller . 
------------------------------------------

 ### Turn off Wifi Power Management
```bash
sudo gedit /etc/NetworkManager/conf.d/default-wifi-powersave-on.conf
```
Added these line below
```conf
[connection]  
wifi.powersave = 2
```
Restart NetworkManager
```bash
sudo systemctl restart NetworkManager
```
### Turn off sleep/suspend mode

Open terminal and run
```bash
sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
```

##  For Gnome 
### Fix Flickering in Ubuntu
```bash
Section "Device"

Identifier "Intel Graphics"
Driver "intel"
Option "AccelMethod" "sna"
Option "TearFree" "true"

EndSection
```

### Add Environment to fix nautlius
[Nautilus Flicker](https://askubuntu.com/questions/1515862/after-upgrade-to-24-04-strange-display-in-nautilus)
### Disable zsh auto_title and alias to open quicky Nvim with fzf

```zsh
## Alias to open file quicky with fzf + neovim
alias nvim = 'nvim $(fzf)'
DISABLE_AUTO_TITLE="true"
function set_terminal_title() {
  echo -en "\e]2;$@\a"
}
```

## KDE
### Install zram
```bash
sudo apt install systemd-zram-generator

```

```bash
sudo nano /etc/systemd/zram-generator.conf
```

``
```bash
// -- Put these 2 lines
[zram0] zram-size = 2048 
compression-algorithm = zstd
```

- Check if **zram** is running
```bash
- cat /proc/swaps
```

---- 
Ref:
- https://support.system76.com/articles/wireless/ -> Disable Power Management of wifi (Internet)
- https://askubuntu.com/questions/473037/how-to-permanently-disable-sleep-suspend -> Turn off sleep/duspend
- https://stackoverflow.com/questions/46721797/how-to-change-the-terminal-title -> Change title terminal
- https://fosspost.org/enable-zram-on-linux-better-system-performance -> Zram