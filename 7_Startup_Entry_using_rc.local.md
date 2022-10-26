## Create rc.local file

[1] Create rc.local file to below path
    sudo nano /etc/rc.local

[2] Paste below script - [Do not forget to replace username]
    #!/bin/sh -e
    #
    # rc.local
    #
    # This script is executed at the end of each multiuser runlevel.
    # Make sure that the script will "exit 0" on success or any other
    # value on error.
    #
    # In order to enable or disable this script just change the execution
    # bits.
    #
    # By default this script does nothing.
    
    DISPLAY=:0 sudo -u kapil bash chromium http://debian.local:1880 --window-size=1920,1080 --start-fullscreen --kiosk --incognito --noerrdialogs --disable-translate --no-first-run --fast --fast-start --disable-infobars --disable-features=TranslateUI --disk-cache-dir=/dev/null  --password-store=basic --no-sandbox --user-data-dir

    exit 0

[3] Save File

[4] Now have to make the file executable with the following command:
    chmod +x /etc/rc.local

[5] Then we need to reload the systemd manager configuration:
    systemctl daemon-reload

[6] Then we start the rc-local daemon:
    systemctl start rc-local
    
[7] And then we check the status of rc-local to confirm it ran OK:
    systemctl status rc-local
    
[8] You should then get an output like below stating the it is active and exited normal:
    ● rc-local.service - /etc/rc.local Compatibility
     Loaded: loaded (/lib/systemd/system/rc-local.service; enabled-runtime; vendor preset: enabled)
    Drop-In: /usr/lib/systemd/system/rc-local.service.d
             └─debian.conf
     Active: active (exited)
       Docs: man:systemd-rc-local-generator(8)
    Process: 58756 ExecStart=/etc/rc.local start (code=exited, status=0/SUCCESS)
    
[9] If status is active, then reboot a system and that's it!!
