# debian-to-do-after-installation
my todos after debian installation

# add username to sudoers
su
nano /etc/sudoers
dodac username ALL=(ALL:ALL) ALL
exit

# add Contrib and Non-Free Repos
sudo nano /etc/apt/sources.list add non-free contrib
sudo apt update
sudo apt upgrade

# stuff
sudo apt install neovim vim default-jdk git zip unzip build-essential nvidia-detect linux-headers-$(uname -r) firmware-linux firmware-linux-nonfree vulkan-tools vulkan-validationlayers unrar gstreamer1.0-vaapi htop bpytop clang cargo libc6-i386 libc6-x32 libu2f-udev samba-common-bin exfat-fuse flatpak timeshift curl

# flatpak
sudo apt install plasma-discover-backend-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

# install flatpaks
sudo flatpak install synologydrive joplin logseq brave firefox

# install nvidia
sudo apt install nvidia-driver
sudo reboot

# battery in laptop
cd ~
mkdir tools
cd tools
git clone https://github.com/AdnanHodzic/auto-cpufreq.git
cd auto-cpufreq
sudo ./auto-cpufreq-installer
sudo auto-cpufreq --install
sudo systemctl status auto-cpufreq
sudo auto-cpufreq --stats

install nerd font

install docker
install docker for deb
systemctl enable docker
system start docker
add user to docker gorup
sudo usermod -aG docker $USER


install zwift

install nvidia container toolkit
curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
  && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
    sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
    sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list

#remove firefox-esr



install display link
install flatpak manager
install anki

fix vim copy paste
