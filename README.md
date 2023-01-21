# This is Unofficial Custom PBRP Recovery Build for Device RMX2020 (Realme C3)
# Made By Me VIVEK DHOK

Custom Recovery Build Commands

For Ubuntu 20. 04 :

# Update Packages.

$ ` sudo apt update `

# Upgrade Packages.

$ sudo apt upgrade

# Install Required Packages.

$ sudo apt install openssh-server screen python git openjdk-8-jdk android-tools-adb bc bison build-essential curl flex g++-multilib gcc-multilib gnupg gperf imagemagick lib32ncurses-dev lib32readline-dev lib32z1-dev liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc yasm zip zlib1g-dev libtinfo5 libncurses5

# install Repo package.

$ sudo wget 'https://storage.googleapis.com/git-repo-downloads/repo' -P /usr/local/sbin/

# Change permissions.

$ sudo chmod +x /usr/local/sbin/repo

# Github Connection.

$ git config --global user.email "GITMAIL" && git config --global user.name "GITUSER"

# Create Folder.

$ mkdir pbrp


#Faced Error Then Used libncurses6 version

