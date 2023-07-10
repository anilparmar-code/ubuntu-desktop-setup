# ubuntu-desktop-setup

````bash
sudo apt update

sudo apt upgrade
````

### Google Chrome

[Download Chrome Deb Package](https://www.google.com/chrome)

```bash
sudo dpkg -i chrome.deb
```

### Tools

````bash
sudo apt install curl git vim make neofetch xclip xsel
````

### Node

````bash
# Install nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
  
# Install latest node version
nvm install node
````


### Zsh

````bash
# Install zsh
sudo apt install zsh -y

# Install OhMyZsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Make default 
chsh -s $(which zsh)

# Restart computer
sudo reboot
````

### List of Zsh Plugins

[ZSH Autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)

### FlatPak
````bash
# Install flatpak
sudo apt install flatpak  

# Gnome plugin flatpak
sudo apt install gnome-software-plugin-flatpak

# Add flatpak repo  
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

# Restart computer  
sudo reboot
````

### FlatPak Software

````bash
# Postman
flatpak install flathub com.getpostman.Postman

# VLC  
flatpak install flathub org.videolan.VLC

# GIMP  
flatpak install flathub org.gimp.GIMP

# Bottles for run windows program  
flatpak install flathub com.usebottles.bottles
````

### Composer

````bash
# install required packages
sudo apt install php-cli unzip

# navigate to home directory
cd ~  

# Download
curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php
  
# Install
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer
````

### Valet Linux+
````bash
# install required packages
sudo apt install network-manager libnss3-tools jq xsel libnss3-tools 

# install php plugins
sudo apt install php-cli php-curl php-mbstring php-xml php-zip

# Valet Linux+
composer global require genesisweb/valet-linux-plus

# add to .zshrc
export PATH="$PATH:$HOME/.config/composer/vendor/bin"

# Install
valet install

## If get error of jq and certutil, install and run valet install again
sudo apt install jq  
sudo apt-get install libnss3-tools
````

### Php Memory Limits
````bash
# navigate to php conf directory
cd /etc/php/8.1/fpm/conf.d

# create new file
sudo nano php-memory-limits.ini

# configuration
memory_limit=1024M
upload_max_filesize=1024M
post_max_size=1024M

# restart valet
valet restart
````

### Mysql

````bash
# Enter Password: 'root'
mysql -u valet -p 

# By default valet linux+ create valet user with password root
# If you want to create or change mysql user valet to root then follow next steps

# *Backup database if you have important database in root user;
# Delete mysql root user
drop user 'root'@'localhost';  

# Create fresh mysql root user;
CREATE USER 'root'@'localhost' IDENTIFIED BY 'root';

# Grant all privileges  
GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost';   
````

### Laravel

````bash
# Laravel Installer
composer global require laravel/installer

# Create test project
laravel new blog
````

### GNOME Extensions
````bash
# chrome extension
sudo apt install chrome-gnome-shell

# Gui GNOME extension manager
sudo apt install gnome-shell-extension-manager
````

### Useful GNOME extensions
1. [PHP Laravel Valet by rahulhaque](https://extensions.gnome.org/extension/4985/php-laravel-valet/)
2. [Net speed Simplified by prateeksu](https://extensions.gnome.org/extension/3724/net-speed-simplified/)
3. [Clipboard History by SUPERCILEX](https://extensions.gnome.org/extension/4839/clipboard-history/)
4. [X11 Gestures by JoseExposito](https://extensions.gnome.org/extension/4033/x11-gestures/)
````bash
# X11 Gestures
sudo add-apt-repository ppa:touchegg/stable

sudo apt update

sudo apt install touchegg

flatpak install flathub com.github.joseexposito.touche
````

### Jetbrains Software
[Toolbox App](https://www.jetbrains.com/toolbox-app/)

### AppImage Launcher
````bash
# Add the PPA via command
sudo add-apt-repository ppa:appimagelauncher-team/stable

sudo apt update
sudo apt install appimagelauncher
````

### Laravel Aliases
````bash
# Add to .zshrc
alias pamf="php artisan migrate:fresh"
alias pamfs="php artisan migrate:fresh --seed"
````