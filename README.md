# ubuntu-desktop-setup

**sudo apt update**  
**sudo apt upgrade**

### Google Chrome
<a href="https://www.google.com/chrome/">Download Chrome Deb Package</a><br>
dpkg -i chrome.deb

### Tools
sudo apt install curl git vim make neofetch xclip xsel

### Node
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash  
nvm install node

npm i -g nodemon

### ZSH
sudo apt install zsh -y  
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"  
chsh -s $(which zsh)  
sudo reboot

### ZSH Plugins
<a href="https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md">ZSH Autosuggestions</a>

### FlatPak
sudo apt install flatpak  
sudo apt install gnome-software-plugin-flatpak  
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo  
sudo reboot

### FlatPak Software
flatpak install flathub com.getpostman.Postman  
flatpak install flathub org.videolan.VLC  
flatpak install flathub org.gimp.GIMP  
flatpak install flathub com.usebottles.bottles

### Composer
sudo apt install php-cli unzip

cd ~  
curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php  
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

### Valet Linux+
sudo apt install network-manager libnss3-tools jq xsel libnss3-tools  
sudo apt install php-cli php-curl php-mbstring php-xml php-zip

composer global require genesisweb/valet-linux-plus

Add <code>export PATH="$PATH:$HOME/.config/composer/vendor/bin"</code> to .zshrc

valet install

**if error jq and certutil install and valet install again**   
sudo apt install jq  
sudo apt-get install libnss3-tools

mysql -u valet -p  
Enter Password: 'root'

drop user 'root'@'localhost';  
CREATE USER 'root'@'localhost' IDENTIFIED BY 'root';  
GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost';

### Laravel
composer global require laravel/installer  
laravel new blog

### Gnome Extentions
sudo apt install chrome-gnome-shell  
sudo apt install gnome-shell-extension-manager

### Gnome extentions
1. <a href="https://extensions.gnome.org/extension/4985/php-laravel-valet/">PHP Laravel Valet by rahulhaque</a>
2. <a href="https://extensions.gnome.org/extension/3724/net-speed-simplified/">Net speed Simplified by prateeksu</a>
3. <a href="https://extensions.gnome.org/extension/4839/clipboard-history/">Clipboard History by SUPERCILEX</a>
4. <a href="https://extensions.gnome.org/extension/4033/x11-gestures/">X11 Gestures by JoseExposito</a>
    - sudo add-apt-repository ppa:touchegg/stable
    - sudo apt update
    - sudo apt install touchegg
    - flatpak install flathub com.github.joseexposito.touche

### Jetbrains Software
<a href="https://www.jetbrains.com/toolbox-app/">Toolbox App</a>