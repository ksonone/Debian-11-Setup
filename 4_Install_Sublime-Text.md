## Install Sublime-Text Code Editor on Debian 11

[1] Update package source list

    echo "deb https://download.sublimetext.com/apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
[2] Fetch package

    wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
[3] Run update Command
    
    sudo apt update
[4] Finally run following command to install Sublime-Text :

    sudo apt install sublime-text

[5] That's it !!
