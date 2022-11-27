## Install Mosquitto Server file

[1] Command to Install Mosquitto Server and Mosquito-Client
    sudo apt install mosuitto mosuitto-clients
    
[2] To Check Status Mosquitto
    sudo systemctl status mosquitto

[3] To Start Mosquitto
    sudo systemctl start mosquitto

[4] To Restart Mosquitto
    sudo systemctl restart mosquitto

[4] To Stop Mosquitto
    sudo systemctl stop mosquitto

[5] Important Tip : In latest mosquitto version to enable mosquitto access globally make following changes to default configuration file

    A. sudo nano /etc/mosquitto/mosquitto.conf

    and add following lines
    
    listener 1883
    allow_anonymous true

    B. Press Ctrl+x and save file

    C. Restart Mosquitto with restart command mentioned in point No. 4

[6] That's it. 