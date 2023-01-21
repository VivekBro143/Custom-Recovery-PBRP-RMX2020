# This is Unofficial Custom PBRP Recovery Build Setup for Device RMX2020 (Realme C3)

<h1 align="center">
  <br>
  <a href="https://pitchblackrecovery.com"><img src="https://raw.githubusercontent.com/shovon668/xda-template/r3/pbrp3-banner-xda.png" alt="Welcome to PitchBlack Recovery Project 👋" width="600"></a>
  <br> </h1>
  
<h4 align="center"> <b> Made By VIVEK DHOK </b> </h4>

# ---^--- Custom Recovery Build Commands ---^---

# For Ubuntu 20. 04 :

# Update Packages.

    sudo apt update

# Upgrade Packages.

    sudo apt upgrade

    sudo apt-get install lib32ncurses-dev 

# Install Required Packages.

    sudo apt install openssh-server screen python git openjdk-8-jdk android-tools-adb bc bison build-essential curl flex g++-multilib gcc-multilib gnupg gperf imagemagick lib32ncurses-dev lib32readline-dev lib32z1-dev liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc yasm zip zlib1g-dev libtinfo5 libncurses5 

If you faced Any Error Then Used libncurses6-dev or latest version in above code 

# Install Repo package.

    sudo wget 'https://storage.googleapis.com/git-repo-downloads/repo' -P /usr/local/sbin/ 

# Change permissions.

    sudo chmod +x /usr/local/sbin/repo 

# Github Connection (Enter Your Details Here)

    git config --global user.email "GITMAIL" && git config --global user.name "GITUSER" 

# Create Folder.

    mkdir pbrp 

    cd pbrp 

# To initialize pitchblack Recovery (Android 11.0) source.

    repo init -u https://github.com/PitchBlackRecoveryProject/manifest_pb -b android-11.0 

# To sync up or downloading the source.

    repo sync 

After repo sync, it will take some time to download your source. Because sources are large in size like 10-20 GB. So wait until it stop downloading.

# Goto Home using ` cd `

    mkdir device_tree_realmec3 

    cd device_tree_realmec3

    git clone https://github.com/sarthakroy2002/device_realme_RMX2020.git

# Rename File 

    mv arrow.dependencies omni.dependencies

# Paste it to Source Device Folder

    cp omni.dependencies /root/pbrp/device/realme/rmx2020 

# First go to Recovery folder for that.

    cd

    cd pbrp 

# Run build script.

    . build/envsetup.sh

# lunch your device. With your device code name like this.

    lunch omni_rmx2020-eng 

# Start your build now.

    mka recoveryimage 

It will start Compiling a Recovery For Your device. It will take 10-20 minutes (it totally depends on your servers CPU and RAM) to build Recovery so wait until 100%.

# If it fails to build:

    export LC_ALL=C 

# Clean first.

    make clobber && make clean && rm -rf out/ 

# Run Build script Step
