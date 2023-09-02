# After Ubuntu install

# VSC : https://code.visualstudio.com/docs/setup/linux

# chrome : 다운로드 후 

# sudo dpkg -i ~/다운로드/google...

# color :
```bash
sudo apt install dconf-editor
gsettings set org.gnome.desktop.background picture-uri ''
gsettings set org.gnome.desktop.background picture-uri-dark ''
gsettings set org.gnome.desktop.background primary-color '#000000'
```

# font
```bash
sudo apt install fonts-firacode
```

# vsc
  # theme : github theme
  # icons : vsc icons

# PX4
```bash
mkdir ~/projects
cd ~/projects
git clone https://github.com/PX4/PX4-Autopilot
PX4-Autopilot/Tools/setup/ubuntu.sh
```

# Humble : https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html

```bash
sudo apt-get install lm-sensors
sudo apt install hardinfo

sudo sensors

#sudo hardinfo
```

# docker
```bash
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
sudo docker run hello-world
```

